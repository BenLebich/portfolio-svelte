<script>
  import { slide } from "svelte/transition";
  //export let innerWidth;
  export let y;
  let heightArrow = 190;
  let hover = false;
  
  let h = 0;
  $: if (!hover) {
    heightArrow = 25;
  } else {
    heightArrow = 190;
  }
  let selected = "Home";
  let sections = ["Home", "About", "Career", "Project", "Contact"];

  function handleClick(e) {
    selected = sections[e.target.getAttribute("data-idx")];
  }

  function enter(e) {
    hover = true;
  }

  function leave(e) {
    hover = false;
  }

  function click(e) {
    hover = !hover;
  }
</script>

<header class="container">
  <img src="/images/xl-logo.png" alt="Ben Lebich Logo" class="main-logo" />
  <div>
    <div
      class="menu"
      style="{(y < 30) ? "" : "position: fixed; margin-top: -30px;"}"
      on:mouseenter={enter}
      on:mouseleave={leave}
      on:click={click}
    >
      <div class="sections" bind:clientHeight={h}>
        {#each sections as section, idx}
          {#if section === selected}
            <div 
              on:click={handleClick}
              data-idx={idx}
              class="{section.toLowerCase()} {section === selected
                ? 'active'
                : ''}"
            >
              {section}
            </div>
          {:else if hover}
            <div
              transition:slide
              on:click={handleClick}
              data-idx={idx}
              class="{section.toLowerCase()} {section === selected
                ? 'active'
                : ''}"
            >
              {section}
            </div>
          {/if}
        {/each}
      </div>

     
    </div>
  </div>
</header>

<style>
  .arrow {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 50%;
  }

  .arrow-head {
    margin-top: -1px;
  }

  .main-logo {
    max-width: 400px;
    height: 100%;
    object-fit: cover;
  }

  header {
    padding-top: 30px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .menu {
    display: flex;
    flex-direction: row;
    margin-left: -87px;
    z-index: 5;
    align-items: flex-start;
  }

  .sections {
    background-color: #ffffff88;
    display: flex;
    flex-direction: column;
    width: 87px;
  }

  .sections div {
    font-size: 25px;
    padding: 2px 7px;
    cursor: pointer;
  }

  .sections div:hover {
    text-decoration: underline;
    text-decoration-color: #dd6031;
  }

  .sections .active {
    color: #ffffff;
    background-color: #171717;
  }

  @media only screen and (max-width: 775px) {
    .main-logo {
      max-width: 200px;
    }
  }
</style>
