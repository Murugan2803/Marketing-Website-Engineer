<script>
  const logos = [
    "../../assets/svelte_logo_pack/haleon.svg",
    "/assets/svelte_logo_pack/kahoot.svg",
    "/assets/svelte_logo_pack/shaadi.svg",
    "/assets/svelte_logo_pack/endeavor.svg",
    "/assets/svelte_logo_pack/nobroker.svg"
  ];
  const loopLogos = [...logos, ...logos];
</script>

<div class="logo-section">
  <div class="line top"></div>
  <div class="slider">
    <div class="fade left"></div>
    <div class="track">
      {#each loopLogos as logo}
        <div class="logo">
          <img src={logo} alt="company logo"/>
        </div>
      {/each}
    </div>
    <div class="fade right"></div>
  </div>
  <div class="line bottom"></div>
</div>

<style>
  .logo-section{
    position:relative;
    background:#050814;
    padding:70px 0;
    overflow:hidden;
  }
  .line{
    position:absolute;
    width:100%;
    height:1px;
    background:#3b4157;
  }
  .top{
    top:0;
  }
  .bottom{
    bottom:0;
  }
  .slider{
    position:relative;
    overflow:hidden;
    width:100%;
  }
  .fade{
    position:absolute;
    top:0;
    width:120px;
    height:100%;
    z-index:2;
    pointer-events:none;
  }
  .fade.left{
    left:0;
    background:linear-gradient(to right,#050814,transparent);
  }
  .fade.right{
    right:0;
    background:linear-gradient(to left,#050814,transparent);
  }
  .track{
    display:flex;
    width:max-content;
    animation:scroll 22s linear infinite;
  }
  .slider:hover .track{
    animation-play-state:paused;
  }
  .logo{
    flex:0 0 auto;
    padding:0 80px;
    display:flex;
    align-items:center;
  }
  .logo img{
    height:42px;
    opacity:.85;
    filter:grayscale(100%);
    transition:.35s;
  }
  .logo img:hover{
    opacity:1;
    filter:grayscale(0%);
    transform:scale(1.1);
  }
  @keyframes scroll{
    from{
      transform:translateX(0);
    }
    to{
      transform:translateX(-50%);
    }
  }
  @media(max-width:768px){
  .logo{
    padding:0 40px;
  }
  .logo img{
    height:32px;
  }
  }
</style>