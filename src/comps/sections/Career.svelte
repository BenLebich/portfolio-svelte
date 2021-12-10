<script>
  import SectionTitle from "../micro/SectionTitle.svelte";
  let heightArrow = 700;
  export let innerWidth;
  
  $: if (innerWidth <= 1000 && innerWidth >= 400) {
      heightArrow = 1000;
  } else if (innerWidth < 400) {
    heightArrow = 1100;
  } else {
    heightArrow = 700;
  }

  let events = [
    {
      range: "Jun - Jul 2016",
      title: "Wordpress Intern",
      place: "RPM National",
      desc: "Leanred how to build WordPress sites.",
      skills: ["WordPress", "HTML", "CSS"]
    },
    {
      range: "Sep 2017 - Jan 2019",
      title: "Wordpress Intern",
      place: "SMC National",
      desc: "Built WordPress sites for clients and rebuilt the theme options.",
      skills: ["WordPress", "PHP", "JavaScript"]
    },
    {
      range: "Sep 2017 - May 2020",
      title: "Computer Science Student",
      place: "Sierra College",
      desc: "Completed all computer science related classes required for Computer Science for Transfer",
      skills: ["Java", "Discrete Structures", "Assembly Language", "C", "Unix/Linux", "Calculus II", "Physics II"]
    },
    {
      range: "Jan 2019 - Current",
      title: "Lead Developer",
      place: "SMC National",
      desc: "Lead the development of a lead to patient tracking application.",
      skills: ["PHP", "MySQL", "jQuery", "Node.js", "MongoDB"]
    }
  ];

  function formatEvent(event, i) {
    return `

    `
  }
</script>

<div class="container">
  <SectionTitle title="Career" />

  {#if innerWidth > 1000}
  <div class="content">
    <div class="left">
        <div class="event ev-1">
            <div class="range">{events[0].range}</div>
            <div class="title">{events[0].title}</div>
            <div class="place">{events[0].place}</div>
            <div class="desc">{events[0].desc}</div>
            <div class="desc">[{events[0].skills.join(", ")}]</div>
        </div>
        <div class="event ev-3">
          <div class="range">{events[2].range}</div>
          <div class="title">{events[2].title}</div>
          <div class="place">{events[2].place}</div>
          <div class="desc">{events[2].desc}</div>
          <div class="desc">[{events[2].skills.join(", ")}]</div>
      </div>
    </div>
    <div class="arrow-desktop">
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
    <div class="right">
        <div class="event ev-2">
          <div class="range">{events[1].range}</div>
          <div class="title">{events[1].title}</div>
          <div class="place">{events[1].place}</div>
          <div class="desc">{events[1].desc}</div>
          <div class="desc">[{events[1].skills.join(", ")}]</div>
        </div>
        <div class="event ev-3">
          <div class="range">{events[3].range}</div>
          <div class="title">{events[3].title}</div>
          <div class="place">{events[3].place}</div>
          <div class="desc">{events[3].desc}</div>
          <div class="desc">[{events[3].skills.join(", ")}]</div>
        </div>
    </div>
  </div>
  {:else}
  <div class="content-mobile">
    <div class="arrow-mobile">
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
    <div class="events">
        <div class="event ev-1">
          <div class="range">{events[0].range}</div>
          <div class="title">{events[0].title}</div>
          <div class="place">{events[0].place}</div>
          <div class="desc">{events[0].desc}</div>
          <div class="desc">[{events[0].skills.join(", ")}]</div>
        </div>
        <div class="event ev-2">
          <div class="range">{events[1].range}</div>
          <div class="title">{events[1].title}</div>
          <div class="place">{events[1].place}</div>
          <div class="desc">{events[1].desc}</div>
          <div class="desc">[{events[1].skills.join(", ")}]</div>
        </div>
        <div class="event ev-3">
          <div class="range">{events[2].range}</div>
          <div class="title">{events[2].title}</div>
          <div class="place">{events[2].place}</div>
          <div class="desc">{events[2].desc}</div>
          <div class="desc">[{events[2].skills.join(", ")}]</div>
        </div>
        <div class="event ev-4">
          <div class="range">{events[3].range}</div>
          <div class="title">{events[3].title}</div>
          <div class="place">{events[3].place}</div>
          <div class="desc">{events[3].desc}</div>
          <div class="desc">[{events[3].skills.join(", ")}]</div>
        </div>
    </div>
  </div>
  {/if}
</div>

<style>
  .arrow-desktop {
      padding-left: 40px;
      padding-right: 40px;
  }

  .arrow-mobile {
      padding-right: 20px;
  }

  .content {
    padding-top: 40px;
    display: flex;
    flex-direction: row;
    justify-content: center;
    text-transform: uppercase;
  }

  .content-mobile {
    padding-top: 40px;
    display: flex;
    flex-direction: row;
    justify-content: center;
    text-transform: uppercase;
  }

  .content-mobile .event {
      padding: 30px 0px;
  }

  .left, .right {
      max-width: 350px;
      padding-top: 30px;
  }

  .event div {
      padding: 5px 0px;
  }

  .content .ev-2 {
      margin-top: 120px;
  }

  .content .ev-3 {
      margin-top: 100px;
  }

  .content .ev-4 {
      margin-top: 100px;
  }

  .range {
      font-size: 38px;
  }

  .title {
      font-size: 26px;
      background-color: #171717;
      color: #ffffff;
      line-height: 16px;
      width: fit-content;

  }
  .place {
      font-size: 25px;
      text-decoration: underline;
      text-decoration-color: #dd6031;

  }
  .desc {
      font-size: 20px;
  }

</style>
