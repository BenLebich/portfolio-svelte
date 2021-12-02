<script>
  import { slide } from "svelte/transition";
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
      <div class="arrow" style="display: none;">
        <svg
          width="18"
          height={heightArrow + 15}
          viewBox="0 0 18 {heightArrow + 15}"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M9 {heightArrow +
              15}L17.6603 {heightArrow}L0.339745 {heightArrow}L9 {heightArrow +
              15}ZM7.5 -6.55671e-08L7.5 {heightArrow + 1.5}L10.5 {heightArrow +
              1.5}L10.5 6.55671e-08L7.5 -6.55671e-08Z"
            fill="#171717"
          />
        </svg>
      </div>
      <div class="arrow">
        <svg
          class="arrow-body"
          width="6"
          height={h}
          viewBox="0 0 6 236"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
          preserveAspectRatio="none"
        >
          <line
            x1="3"
            y1="1.31134e-07"
            x2="2.99999"
            y2="236"
            stroke="#171717"
            stroke-width="6"
          />
        </svg>
        <svg
          class="arrow-head"
          width="24"
          height="20"
          viewBox="0 0 24 20"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M12 20L0.741669 0.5H23.2583L12 20Z" fill="#171717" />
        </svg>
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
    position: fixed;
    margin-left: -122.5px;
    z-index: 5;
    align-items: flex-start;
  }

  .sections {
    margin-right: 20px;
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
