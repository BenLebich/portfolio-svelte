<script>
    export let y;
    export let innerWidth;
    $: console.log(innerWidth)
    let leftLight = 0;
    let leftDark = 0;
    
    $: leftLight = y * .4;
    $: leftDark = y * .6;

    let widths = 20;
    $: widths = Math.round(y / 10);
</script>

<section >
    <div class="mountains-top">
        <div class="range lighter" style="margin-left: {leftLight}px">
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
        <div class="range darker" style="margin-left: -{leftDark}px"> 
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
            content
        </div>
    </div>
    <!--
    <div class="mountains-bottom">
        <div style="width: {widths}%">
            <svg  width="1250" height="174" viewBox="0 0 1250 174" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M0 134.875L52.0833 173.176L104.167 19.9745L156.25 77.4249L208.333 96.5751L260.417 173.176L312.5 77.4249H364.583L416.667 58.2748L468.75 173.176L520.833 154.025L572.917 96.5751L625 115.725L677.083 134.875H729.167L781.25 19.9745L833.333 154.025L885.417 58.2748L937.5 96.5751L989.583 154.025L1041.67 39.1247L1093.75 77.4249L1145.83 39.1247L1197.92 96.5751L1250 77.4249V0.8244H1197.92H1145.83H1093.75H1041.67H989.583H937.5H885.417H833.333H781.25H729.167H677.083H625H572.917H520.833H468.75H416.667H364.583H312.5H260.417H208.333H156.25H104.167H52.0833H0V134.875Z" fill="url(#paint0_linear_49_14)"/>
                <defs>
                <linearGradient id="paint0_linear_49_14" x1="0" y1="0.824402" x2="0" y2="173.176" gradientUnits="userSpaceOnUse">
                <stop stop-color="#DD6031"/>
                <stop offset="1" stop-color="#DD6031"/>
                </linearGradient>
                </defs>
                </svg>
        </div>
        <div style="width: {100-widths}%">
            <svg width="1250" height="174" viewBox="0 0 1250 174" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1250 134.875L1197.92 173.176L1145.83 19.9745L1093.75 77.4249L1041.67 96.5751L989.583 173.176L937.5 77.4249H885.417L833.333 58.2748L781.25 173.176L729.167 154.025L677.083 96.5751L625 115.725L572.917 134.875H520.833L468.75 19.9745L416.667 154.025L364.583 58.2748L312.5 96.5751L260.417 154.025L208.333 39.1247L156.25 77.4249L104.167 39.1247L52.0833 96.5751L-3.8147e-05 77.4249V0.8244H52.0833H104.167H156.25H208.333H260.417H312.5H364.583H416.667H468.75H520.833H572.917H625H677.083H729.167H781.25H833.333H885.417H937.5H989.583H1041.67H1093.75H1145.83H1197.92H1250V134.875Z" fill="url(#paint0_linear_56_17)"/>
                <defs>
                <linearGradient id="paint0_linear_56_17" x1="1250" y1="0.824402" x2="1250" y2="173.176" gradientUnits="userSpaceOnUse">
                <stop stop-color="#DD6031"/>
                <stop offset="1" stop-color="#DD6031"/>
                </linearGradient>
                </defs>
                </svg>
        </div>
            
                
    </div>

        -->

</section>
<style>
  .mountains-top {
    padding-top: 300px;
    width: 100vw;
    position: relative;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .mountains-top .range {
      width: 300%;
      height: 300px;
      display: flex;
    flex-direction: row;
  }

  .mountains-top svg {
      width: 300%;
      height: 300px;
  }
  .mountains-top .darker {
      margin-top: -300px;
  }
  .content {
    text-align: center;
    background-color: #DD6031;
    padding: 200px 100px;
  }

  .mountains-bottom {
      display: flex;
  }
</style>
