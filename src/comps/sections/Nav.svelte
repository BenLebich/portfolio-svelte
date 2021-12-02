<script>
  export let innerWidth;
  let heightArrow = 190;
  if (innerWidth <= 775) {
    heightArrow = 25;
  }
  let selected = "Home";
  let sections = ["Home", "About", "Career", "Project", "Contact"];

  function handleClick(e) {
    selected = sections[e.target.getAttribute("data-idx")];
  }
</script>

<header class="container">
  <img src="/images/xl-logo.png" alt="Ben Lebich Logo" class="main-logo" />
  <div>
    <div class="menu">
      <div class="sections">
        {#each sections as section, idx}
          {#if innerWidth <= 775 && section === selected}
            <div
              on:click={handleClick}
              data-idx={idx}
              class="{section.toLowerCase()} {section === selected
                ? 'active'
                : ''}"
            >
              {section}
            </div>
          {:else if innerWidth > 775}
            <div
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
      <div class="arrow">
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
    </div>
  </div>
</header>

<style>
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
  }

  .sections {
    margin-right: 20px;
    background-color: #ffffff88;
  }

  .sections div {
    font-size: 25px;
    padding: 2px 7px;
    cursor: pointer;
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
