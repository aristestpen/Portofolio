<style scoped>
    body {
      margin-top: 35px;
    }
    .support-palestine,
    .support-palestine:visited {
      position: inherit;
      /* left: 0;
      top: 0;
      right: 0; */
      /* background: rgb(0, 0, 0); */
      display: flex;
      justify-content: center;
      padding-top: 5px;
      padding-bottom: 5px;
      z-index: 10000;
      text-decoration: none;
      font-family: arial;
      margin-bottom: 20px
    }
    .support-palestine:hover,
    .support-palestine:active {
      /* background: black; */
      display: flex;
      /* background: rgb(80, 80, 80); */
      text-decoration: none;
    }
    .support-palestine__flag {
      margin-right: 10px;
    }
  
    .support-palestine__label {
      color: white;
      font-size: 12px;
      line-height: 24px;
    }
    .background {
      background: darkgreen;
  
      height: 21px;
    }
    .top {
      background: black;
      width: 40px;
      height: 8px;
      z-index: 1;
    }
    .middle {
      background: white;
      width: 100%;
      height: 8px;
      z-index: 1;
    }
    .triangle {
      background: auto;
      border-top: 12px solid transparent;
      border-bottom: 12px solid transparent;
      border-left: 20px solid red;
      z-index: 2;
      position: relative;
      top: -16px;
      left: 0;
    }
  </style>
  
  <template>
    <div>
      <a
    class="support-palestine"
    href="https://kitabisa.com/campaign/celenganwargapalestina/"
    target="_blank"
    rel="nofollow noopener"
    title="Donate to support palestine"
  >
    <div
      class="support-palestine__flag"
      role="img"
      aria-label="Flag of palestine"
    >
      <div class="background">
        <div class="top"></div>
        <div class="middle"></div>
        <div class="triangle"></div>
      </div>
    </div>
    <div class="support-palestine__label">Donate to support Palestine</div>
  </a>
    </div>
  </template>