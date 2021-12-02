<script>
  import SectionTitle from "./SectionTitle.svelte";
</script>

<SectionTitle title="About"/>
<div class="content">
  <img src="/images/me.png" alt="Ben Lebich Hiking" />
  <div class="desc">
    <span class="name">ben</span><br />
    Archer<br />
    backpacker<br />
    weightlifter<br />
    Programmer<br />
    Javascript<br />
    MongoDb<br />
    Node.js<br />
    jquery<br />
    PHP<br />
  </div>
</div>

<style>
  .content {
    display: flex;
    justify-content: center;
    padding-top: 50px;
  }
  img {
    width: 300px;
    height: 100%;
    object-fit: cover;
    padding-right: 10px;
  }
  .desc {
    padding-left: 10px;
    width: 300px;
    color: #ffffff;
    text-transform: uppercase;
    text-align: left;
    font-size: 42px;
  }
  .name {
    font-size: 60px;
    text-decoration: underline;
    line-height: 50px;
  }

  @media only screen and (max-width: 775px) {
    img {
    width: 150px;
  }
  .desc {
    width: 150px;
  font-size: 20px;
  }
  .name {
    font-size: 30px;
    line-height: 25px;
  }
  }
</style>
