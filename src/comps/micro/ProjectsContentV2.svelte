<script>
import { prop_dev } from "svelte/internal";

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
      name: "Door Sim",
      desc: `Custom door simulator I built for a door installation company. 
      The hardest part for this task was learning how to skew an image in Javascript.`,
      img: "/images/projects/sim2.jpeg",
      stack: ["Next.js", "Canvas2D", "Skewing"],
      read: false,
    },
    {
      name: "Construction",
      desc: `Rebuild for a general contracter. Previously it used Elementor and
      had minimal design consitency. It needed a face lift to something more modern.`,
      link: "https://millsawconstruction.com",
      img: "/images/projects/millsaw.jpeg",
      stack: ["Next.js", "Swiper.js", "Netlify"],
      read: false,
    },
    {
      name: "Creative",
      desc: `Build for a Videographer. This was my first time building a horizontal sliding website and second time using Svelte.`,
      link: "https://dannymatthews.net/",
      img: "/images/projects/danny.jpeg",
      stack: ["SvelteKit", "Swipper.js", "Netlify"],
      read: false,
    },
    {
      name: "Farming Tech",
      desc: `Rebuild for a seaweed business. Previously it had a poor outdated design.
      For this project we contracted out a UI/UX designer and used Elementor to allow them to maintain the site.`,
      link: "https://seaweedtechnologies.no/",
      img: "/images/projects/seaweed.jpeg",
      stack: ["WordPress", "Elementor"],
      read: false,
    },
    {
      name: "Waste Tech",
      desc: `Build from the ground up for a start up garbage business in Norway.
      The goal of the site was to show a proof of concept to investors.`,
      link: "https://avfallsplassen.com/",
      img: "/images/projects/trash.jpeg",
      stack: ["Wordpress", "Elementor"],
      read: false,
    },
    {
      name: "Recreation",
      desc: `Rebuild for a axe throwing business. 
      Their old site had almost no design consistency and needed a redesign.`,
      link: "https://getaxed.web.app/",
      img: "/images/projects/axe.jpeg",
      stack: ["React.js", "Tailwind", "Firebase"],
      read: false,
    },
  ];

  $: {
    console.log(projects);
  }
</script>

<SectionTitle title="Projects" />
<div class="content">
  <div class="projects">
    {#each projects as proj}
      <div class="project">
        <div class="info">
          <h4 class="name">
            {proj.name}
          </h4>
          <div class="stack">
            {#each proj.stack as stack}
              <p>{stack}</p>
            {/each}
          </div>
        </div>
        <div class="triangle" />
        <div class="trimobile" />
        <div class="img">
          <div class={"desc" + (proj.read ? " showdesc" : "")}>
            <p>
              {proj.desc}
            </p>
          </div>
          <img src={proj.img} alt="{proj.name} Screenshot" />
          <h5 class="read" on:click={() => {proj.read = !proj.read}}>
            {#if proj.read}
              Read Less
            {:else}
              Read More
            {/if}
          </h5>
          {#if proj.link}
            <a href={proj.link} target="_blank">
              <h5 class="learn">
                View Project <svg
                  width="22"
                  height="8"
                  viewBox="0 0 22 8"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M21.3536 4.35355C21.5488 4.15829 21.5488 3.84171 21.3536 3.64645L18.1716 0.464466C17.9763 0.269204 17.6597 0.269204 17.4645 0.464466C17.2692 0.659728 17.2692 0.976311 17.4645 1.17157L20.2929 4L17.4645 6.82843C17.2692 7.02369 17.2692 7.34027 17.4645 7.53553C17.6597 7.7308 17.9763 7.7308 18.1716 7.53553L21.3536 4.35355ZM0 4.5L21 4.5V3.5L0 3.5L0 4.5Z"
                    fill="white"
                  />
                </svg>
              </h5>
            </a>
          {/if}
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

  .info {
    display: flex;
  }

  .info .stack {
    display: flex;
    gap: 5px;
    flex-direction: center;
    align-items: center;
    margin-left: 5px;
  }

  .info .stack p {
    margin-bottom: 0px;
    background-color: #171717;
    color: #fff;
    text-transform: uppercase;
    padding: 0px 5px;
  }

  .info .name {
    width: fit-content;
    background-color: #dd6031;
    color: #fff;
    text-transform: uppercase;
    margin-bottom: 0px;
    padding: 10px 5px;
    font-size: 18px;
  }

  .projects {
    flex-direction: column;
    gap: 50px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
  }

  .project {
    background-color: transparent;
  }

  .img {
    max-height: 500px;
    width: 100%;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.14);
    overflow: hidden;
    border: 2px solid #dd6031;
    position: relative;
  }

  .img:before {
    content: "";
    position: absolute;
    top: 0px;
    left: 0px;
    right: 0px;
    bottom: 0px;
    background: #171717;
    background: linear-gradient(0deg, rgba(255,255,255,1) 0%, rgba(23,23,23,1) 100%);
    opacity: 0.2;
    
  }

  .desc {
    position: absolute;
    top: -100%;
    visibility: hidden;
    transition: all 300ms ease;
    background-color: #fff;
    margin: 30px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.14);
  }

  .desc p {
    padding: 30px;
    font-size: 20px;
    margin-bottom: 0px;
    text-align: left;

  }

  .showdesc {
    top: 0px;
    visibility: visible;
  }

  .read,
  .learn {
    position: absolute;
    bottom: 15px;
    color: white;
    background-color: #171717;
    padding: 10px 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    width: fit-content;
    margin-bottom: 0px;
    cursor: pointer;
  }

  .read {
    left: 15px;
  }

  .learn {
    right: 15px;
  }

  .img img {
    width: 100%;
    object-fit: cover;
    height: 100%;
    object-position: top;
  }

  @media (max-width: 1200px) {
    .projects {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media (max-width: 680px) {
    .projects {
      grid-template-columns: 1fr;
    }
  }
</style>
