<script>
  import { slide } from "svelte/transition";
  //export let innerWidth;
  export let y;
  export let innerWidth;
  let hover = false;
  let yMin = 30;

  $: if (innerWidth > 775) {
    yMin = 60
  } else {
    yMin = 30;
  }

  let selected = "Home";
  let sections = ["Home", "About", "Career", "Project", "Contact"];

  function handleClick(e) {
    selected = sections[e.target.getAttribute("data-idx")];
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
      style={y < yMin ? "" : " position: fixed; margin-top: -30px;"}
      on:click={click}
    >
      <div class="sections">
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

              {#if hover === false}
                <svg
                  width="9"
                  height="7"
                  viewBox="0 0 9 7"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path d="M4.5 7L0.602886 0.25H8.39711L4.5 7Z" fill="white" />
                </svg>
              {/if}
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
              {#if hover === true && idx === 0 && false}
                <svg
                  width="9"
                  height="7"
                  viewBox="0 0 9 7"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path d="M4.5 7L0.602886 0.25H8.39711L4.5 7Z" fill="black" />
                </svg>
              {/if}
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
    margin-left: -100px;
    margin-top: 30px;
    z-index: 5;
    align-items: flex-start;
    position: absolute;
  }

  .sections {
    background-color: #ffffff88;
    display: flex;
    flex-direction: column;
    max-width: 100px;
    height: 100%;
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
      max-width: 185px;
    }

    .menu {
      margin-top: 0px;
    }
  }
</style>
