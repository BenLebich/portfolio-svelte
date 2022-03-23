<script>
  import SectionTitle from "./SectionTitle.svelte";

  const projects = [
    /*{
      name: "SMC National",
      desc: `Dental marketing dashboard that I built for SMC National. 
      The purpose of this app was to simplify reporting and provide a lead to patient tracking and performance tracking.`,
      link: "https://smcnational.com/",
      img: "/images/project-6.png",
      stack: ["PHP", "jQuery", "Node.js", "Mongodb", "Aptible"]
    },*/
    {
      name: "Danny Matthews",
      desc: `Build for a Videographer. This was my first time building a horizontal sliding website and second time using Svelte.`,
      link: "https://dannymatthews.net/",
      img: "/images/project-7.png",
      stack: ["SvelteKit", "Swipper.js", "Netlify"],
    },
    {
      name: "SoftSeaweed",
      desc: `Rebuild for a seaweed business. Previously it had a poor outdated design.
      For this project we contracted out a UI/UX designer and used Elementor to allow them to maintain the site.`,
      link: "https://seaweedtechnologies.no/",
      img: "/images/project-4.png",
      stack: ["WordPress", "Elementor"],
    },
    {
      name: "Millsaw Construction",
      desc: `Rebuild for a general contracter. Previously it used Elementor and
      had minimal design consitency. It needed a face lift to something more modern.`,
      link: "https://eloquent-heyrovsky-2eae78.netlify.app/",
      img: "/images/project-1.png",
      stack: ["Next.js", "Swiper.js", "Netlify"],
    },
    {
      name: "Avfallsplassen",
      desc: `Build from the ground up for a start up garbage business in Norway.
      The goal of the site was to show a proof of concept to investors.`,
      link: "https://avfallsplassen.com/",
      img: "./images/project-3.png",
      stack: ["Wordpress", "Elementor"],
    },
    {
      name: "Get Axed",
      desc: `Rebuild for a axe throwing business. 
      Their old site had almost no design consistency and needed a redesign.`,
      link: "https://getaxed.web.app/",
      img: "./images/project-2.png",
      stack: ["React.js", "Tailwind", "Firebase"],
    },
    {
      name: "Ben's Calendar",
      desc: `Calendar app that I built for myself to learn and experiment with Firebase + React. 
      The database is currently turned off so it's not 100% functional.`,
      link: "https://ben-calendar.web.app/",
      img: "./images/project-5.png",
      stack: ["React.js", "Firebase"],
    },
  ];
</script>

<SectionTitle title="Projects" />
<div class="content">
  <div class="cards">
    {#each projects as proj, i}
      <div class="card">
        <div class="info">
          <div class="name">
            {proj.name}
          </div>
          <div class="desc">
            {proj.desc}
          </div>
          <div class="stack">
            [
            {proj.stack.join(", ")}
            ]
          </div>
          <a class="link" href={proj.link} target="_blank"> View Project </a>
        </div>
        <div class="triangle">
        </div>
        <div class="trimobile">
          
        </div>
        <div class="img">
          <img src={proj.img} alt="{proj.name} Screenshot" />
        </div>
      </div>
    {/each}
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
    flex-direction: column;
  }
  .card {
    margin: 70px;
    display: flex;
    flex-direction: row;
    filter: drop-shadow(0px 2px 5px rgba(0, 0, 0, 0.25));
  }

  .card .info {
    padding: 50px;
    text-transform: uppercase;
    text-align: left;
    z-index: 4;
  }

  .card .name {
    text-align: center;
    background-color: #dd6031;
    width: 350px;
    color: white;
    font-size: 25px;
    margin-left: -65px;
    line-height: 30px;
  }

  .card .desc {
    font-size: 20px;
    text-align: left;
    margin-top: 50px;
    margin-bottom: 50px;
  }

  .card .stack {
    margin-bottom: 50px;
    font-size: 20px;
  }

  .card .link {
    color: black;
    font-size: 25px;
  }

  .card img {
    width: 550px;
    height: 100%;
    filter: grayscale(85%);
    object-fit: cover;
  }

  .card .triangle svg {
    height: 100%;
    width: 37px;
    z-index: 3;
    margin-right: -35px;
  }

  .card .triangle {
    z-index: 3;
  }

  .card .trimobile {
    z-index: 3;
    display: none;
  }

  .card .trimobile svg {
    z-index: 3;
  }

  .card:nth-child(even) {
    margin-right: 120px;
  }
  .card:nth-child(odd) {
    margin-left: 120px;
  }

  @media only screen and (max-width: 1400px) {
    .card img {
      width: 450px;
    }
  }

  @media only screen and (max-width: 1050px) {
    .card img {
      width: 350px;
    }
  }

  @media only screen and (max-width: 950px) {
    .card img {
      width: 300px;
    }
  }

  @media only screen and (max-width: 900px) {
    .card img {
      height: 500px;
      width: 100%;
    }

    .card {
      flex-direction: column;
    }

    .card:nth-child(even) {
      margin-right: 20px;
      margin-left: 20px;
    }
    .card:nth-child(odd) {
      margin-right: 20px;
      margin-left: 20px;
    }

    .card .trimobile {
      display: block;
    }

    .card .trimobile svg {
      width: 100%;
      height: 37px;
      margin-bottom: -52px;
    }

    .card .triangle {
      display: none;
    }
  }

  @media only screen and (max-width: 500px) {
    .card .info {
      padding: 20px;
    }

    .card .desc {
      margin-top: 30px;
      margin-bottom: 30px;
    }

    .card .stack {
      margin-bottom: 30px;
    }

    .card .name {
      margin-left: -30px;
      max-width: 270px;
    }

    .card img {
      height: 350px;
    }
  }

  @media only screen and (max-width: 400px) {

    .card .name {
      margin-left: -30px;
      max-width: 200px;
      font-size: 20px;
      line-height: 25px;

    }

    .card .desc, .card .stack, .card .link {
      font-size: 15px;
    }



    .card img {
      height: 300px;
    }
    
  }
</style>
