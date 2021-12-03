<script>
    export let y;
    export let innerWidth;
    let leftLight = 0;
    let leftDark = 0;
  
    $: leftLight = y * 0.4;
    $: leftDark = y * 0.6;
  
    let widths = 20;
    $: widths = Math.round(y / 10);
    import ContactContent from '../micro/ContactContent.svelte';
  
  </script>
  
  <section>
    <div class="mountains">
        <div class="range lighter" style="margin-left: -{leftLight - 2800}px">
          <svg
            width="2500"
            height="382"
            viewBox="0 0 2500 382"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="none"
            style="transform: scale(-1,1)"
          >
            <path
              d="M0 229.2H104.167L208.333 38.2L312.5 152.8H416.667L520.833 0L625 114.6L729.167 267.4L833.333 38.2L937.5 305.6L1041.67 229.2L1145.83 267.4L1250 191L1354.17 76.4L1458.33 0L1562.5 38.2L1666.67 114.6L1770.83 0L1875 114.6L1979.17 152.8L2083.33 114.6L2187.5 267.4L2291.67 305.6L2395.83 0L2500 114.6V382H2395.83H2291.67H2187.5H2083.33H1979.17H1875H1770.83H1666.67H1562.5H1458.33H1354.17H1250H1145.83H1041.67H937.5H833.333H729.167H625H520.833H416.667H312.5H208.333H104.167H0V229.2Z"
              fill="url(#paint0_linear_49_16)"
            />
            <defs>
              <linearGradient
                id="paint0_linear_49_16"
                x1="0"
                y1="382"
                x2="0"
                y2="0"
                gradientUnits="userSpaceOnUse"
              >
                <stop stop-color="#E2E2E2" />
                <stop offset="1" stop-color="#E2E2E2" />
              </linearGradient>
            </defs>
          </svg>
    
          {#if innerWidth > 1400}
            <svg
              width="2500"
              height="382"
              viewBox="0 0 2500 382"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              preserveAspectRatio="none"
            >
              <path
                d="M0 229.2H104.167L208.333 38.2L312.5 152.8H416.667L520.833 0L625 114.6L729.167 267.4L833.333 38.2L937.5 305.6L1041.67 229.2L1145.83 267.4L1250 191L1354.17 76.4L1458.33 0L1562.5 38.2L1666.67 114.6L1770.83 0L1875 114.6L1979.17 152.8L2083.33 114.6L2187.5 267.4L2291.67 305.6L2395.83 0L2500 114.6V382H2395.83H2291.67H2187.5H2083.33H1979.17H1875H1770.83H1666.67H1562.5H1458.33H1354.17H1250H1145.83H1041.67H937.5H833.333H729.167H625H520.833H416.667H312.5H208.333H104.167H0V229.2Z"
                fill="url(#paint0_linear_49_16)"
              />
              <defs>
                <linearGradient
                  id="paint0_linear_49_16"
                  x1="0"
                  y1="382"
                  x2="0"
                  y2="0"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#E2E2E2" />
                  <stop offset="1" stop-color="#E2E2E2" />
                </linearGradient>
              </defs>
            </svg>
          {/if}
        </div>
        <div class="range darker" style="margin-left: {leftDark - 2800}px; z-index: 2;">
          <svg
            width="2500"
            height="382"
            viewBox="0 0 2500 382"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="none"
            style="transform: scale(-1,1)"
          >
            <path
              d="M0 114.6L104.167 38.2L208.333 343.8L312.5 229.2L416.667 191L520.833 38.2L625 229.2H729.167L833.333 267.4L937.5 38.2L1041.67 76.4L1145.83 191L1250 152.8L1354.17 114.6H1458.33L1562.5 343.8L1666.67 76.4L1770.83 267.4L1875 191L1979.17 76.4L2083.33 305.6L2187.5 229.2L2291.67 305.6L2395.83 191L2500 229.2V382H2395.83H2291.67H2187.5H2083.33H1979.17H1875H1770.83H1666.67H1562.5H1458.33H1354.17H1250H1145.83H1041.67H937.5H833.333H729.167H625H520.833H416.667H312.5H208.333H104.167H0V114.6Z"
              fill="url(#paint0_linear_49_13)"
            />
            <defs>
              <linearGradient
                id="paint0_linear_49_13"
                x1="0"
                y1="382"
                x2="0"
                y2="38.2"
                gradientUnits="userSpaceOnUse"
              >
                <stop stop-color="#DD6031" />
                <stop offset="1" stop-color="#DD6031" />
              </linearGradient>
            </defs>
          </svg>
          {#if innerWidth > 1400}
            <svg
              width="2500"
              height="382"
              viewBox="0 0 2500 382"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              preserveAspectRatio="none"
              
            >
              <path
                d="M0 114.6L104.167 38.2L208.333 343.8L312.5 229.2L416.667 191L520.833 38.2L625 229.2H729.167L833.333 267.4L937.5 38.2L1041.67 76.4L1145.83 191L1250 152.8L1354.17 114.6H1458.33L1562.5 343.8L1666.67 76.4L1770.83 267.4L1875 191L1979.17 76.4L2083.33 305.6L2187.5 229.2L2291.67 305.6L2395.83 191L2500 229.2V382H2395.83H2291.67H2187.5H2083.33H1979.17H1875H1770.83H1666.67H1562.5H1458.33H1354.17H1250H1145.83H1041.67H937.5H833.333H729.167H625H520.833H416.667H312.5H208.333H104.167H0V114.6Z"
                fill="url(#paint0_linear_49_13)"
              />
              <defs>
                <linearGradient
                  id="paint0_linear_49_13"
                  x1="0"
                  y1="382"
                  x2="0"
                  y2="38.2"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#DD6031" />
                  <stop offset="1" stop-color="#DD6031" />
                </linearGradient>
              </defs>
            </svg>
          {/if}
        </div>
      </div>
    <div class="content">
      <div class="container">
          <ContactContent />
      </div>
    </div>
  </section>
  
  <style>
    .mountains {
      width: 100vw;
      position: relative;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      background-color: #E2E2E2;
    }
    .mountains .range {
      width: 300%;
      height: 150px;
      display: flex;
      flex-direction: row;
    }
    .mountains .lighter {
        height: 200px;
    }
    .mountains svg {
      width: 300%;
      height: 150px;
    }
    .mountains .lighter svg {
        height: 200px;
    }
    .content {
      text-align: center;
      background-color: #dd6031;
      padding: 100px 0px 0px 0px;
    }
  </style>
  