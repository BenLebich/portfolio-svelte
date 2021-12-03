<script>
  import SectionTitle from "./SectionTitle.svelte";


  let cardWidths = [5, 5, 5];

  function changeWidth(e) {
    let card = parseInt(e.target.getAttribute("data-card"));
    console.log(e);
    console.log(card);
    if (cardWidths[card] === 5) {
      cardWidths[card] = 95;
    } else {
      cardWidths[card] = 5;
    }
    console.log(cardWidths);
  }
</script>

<SectionTitle title="Projects" />
<div class="content">
  <div class="cards">
    <div class="card" on:click={changeWidth}>
      <div class="info" data-card="0">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud
      </div>
      <img
        style="width: {cardWidths[0]}%; transition: width 300ms ease-in-out;"
        src="/images/project-1.png"
        alt="Millsaw Construction"
        data-card="0"
      />
    </div>
    <div class="card" on:click={changeWidth}>
      <div class="info" data-card="1">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud
      </div>
      <img
        style="width: {cardWidths[1]}%; transition: width 300ms ease-in-out;"
        src="/images/project-2.png"
        alt="Millsaw Construction"
        data-card="1"
      />
    </div>
    <div class="card" on:click={changeWidth}>
      <div class="info" data-card="2">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud
      </div>
      <img
        style="width: {cardWidths[2]}%; transition: width 300ms ease-in-out;"
        src="/images/project-3.png"
        alt="Millsaw Construction"
        data-card="2"
      />
    </div>
  </div>
</div>

<style>
  .content {
    display: flex;
    justify-content: center;
    padding-top: 50px;
  }
  .cards {
    display: flex;
    flex-direction: row;
  }
  .card {
    margin: 10px;
    display: flex;
    flex-direction: row;
  }

  .info {
    padding: 5%;
    height: 400px;
    padding-left: 10%;
  }

  img {
    height: 400px;
    object-fit: cover;
    position: absolute;
    filter: saturate(0);
  }

  @media only screen and (max-width: 1200px) {
    .cards {
      flex-direction: column;
    }
  }
</style>
