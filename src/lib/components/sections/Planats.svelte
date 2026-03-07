<script>
  import imageURL from "../../assets/Mask group.png";
</script>

<section class="hero">
  <div class="icon-wrapper">
    <div class="icon-box">
      <div class="icon-inner">
        <img src={imageURL} alt="CometChat Logo" />
      </div>
    </div>
  </div>
  <div class="planet-wrapper">
    <div class="glow"></div>
    <div class="planet"></div>
  </div>
  <div class="content">
    <div class="title-group">
      <h1>
        You don’t need to build it
        <br /> all to ship it all
      </h1>
    </div>
    <p class="description">
      Start with chat. Or go full stack. Build fast, scale securely, and <br />
      focus on what your agent does - not what it’s missing.
    </p>
  </div>
  <div class="cta">
    <button class="btn-outline">Talk to Us</button>
    <button class="btn-primary">
      Try the Agent Builder
    </button>
  </div>
</section>

<style>
  .hero {
    background: #070614;
    min-height: 850px;
    text-align: center;
    overflow: hidden;
    position: relative;
    font-family: system-ui;
  }
  .icon-wrapper {
    display: flex;
    justify-content: center;
    margin-bottom: 40px;
    position: relative;
    z-index: 3;
  }
  .icon-box {
    width: 150px;
    height: 140px;
    border-radius: 22px;
    border: 2px solid rgba(120, 90, 255, 0.6);
    /* .icon-wrapper {
      display: flex;
      justify-content: center;
      margin-bottom: 40px;
      position: relative;
      z-index: 3;
    } */
    box-shadow:
      inset 0 0 20px rgba(120, 90, 255, 0.35),
      0 0 40px rgba(120, 90, 255, 0.25);
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .icon-inner img {
    width: 73px;
    height: 74px;
    object-fit: contain;
  }
  .planet-wrapper {
    position: relative;
    height: 150px;
    z-index: 1;
  }
  .glow {
    position: absolute;
    top: 10px;
    left: 50%;
    transform: translateX(-50%);
    width: 900px;
    height: 200px;
    background: radial-gradient(
      ellipse at center,
      rgba(120, 90, 255, 0.7) 0%,
      rgba(120, 90, 255, 0.35) 40%,
      transparent 70%
    );
    filter: blur(80px);
  }
  .title-group h1 {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 500;
    font-size: clamp(20px, 3vw, 36px);
    line-height: 110%;
    letter-spacing: 0.009em;
    color: #fafaff;
    margin: 0;
  }
  .planet {
    position: absolute;
    top: 80px;
    left: 50%;
    transform: translateX(-50%);
    width: 2000px;
    height: 1000px;
    background: #070614;
    border-radius: 1000px 1000px 0 0;
  }
  .content {
    max-width: 720px;
    margin: auto;
    padding-top: 0px;
    position: relative;
    z-index: 3;
  }
  p {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 400;
    font-size: clamp(14px, 1.6vw, 16px);
    line-height: 120%;
    letter-spacing: 0.009em;
    color: #fafaff;
    opacity: 0.74;
    margin-top: 20px;
  }
  .cta {
    font-family: "Satoshi Variable", sans-serif;
    margin-top: 32px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 14px;
    flex-wrap: wrap;
    position: relative;
    z-index: 3;
  }
  .btn-outline {
    padding: 12px 22px;
    border-radius: 14px;
    font-size: 14px;
    cursor: pointer;
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(255,255,255,0.18);
    color: #ffffff;
    transition: all 0.25s ease;
  }
  .btn-outline:hover {
    background: rgba(111,92,255,0.35);
    border-color: rgba(255,255,255,0.35);
  }
  .btn-primary {
    padding: 12px 24px;
    border-radius: 14px;
    font-size: 14px;
    cursor: pointer;
    border: none;
    color: white;
    background: linear-gradient(
      135deg,
      #6f5cff 0%,
      #8b7bff 50%,
      #a594ff 100%
    );
    box-shadow:
      0 6px 20px rgba(111,92,255,0.35),
      inset 0 1px 0 rgba(255,255,255,0.15);
    transition: all 0.25s ease;
  }
  .btn-primary:hover {
    transform: translateY(-2px);
    box-shadow:
      0 10px 30px rgba(111,92,255,0.5),
      inset 0 1px 0 rgba(255,255,255,0.2);
  }
  @media (max-width: 1024px) {
    .hero {
      min-height: 750px;
      padding: 60px 20px 0;
    }
    .icon-box {
      width: 130px;
      height: 120px;
    }
    .icon-inner img {
      width: 60px;
      height: 60px;
    }
    .planet {
      width: 1400px;
      height: 700px;
      top: 70px;
    }
    .glow {
      width: 700px;
      height: 180px;
    }
    .content {
      max-width: 600px;
    }
  }
  @media (max-width: 768px) {
    .hero {
      min-height: 650px;
      padding: 50px 16px 0;
    }
    .icon-box {
      width: 110px;
      height: 105px;
      border-radius: 18px;
    }
    .icon-inner img {
      width: 50px;
      height: 50px;
    }
    .planet-wrapper {
      height: 120px;
    }
    .planet {
      width: 1100px;
      height: 550px;
      top: 60px;
    }
    .glow {
      width: 500px;
      height: 150px;
      filter: blur(60px);
    }
    .content {
      padding: 0 10px;
    }
    .description br {
      display: none;
    }
    .cta {
      flex-direction: column;
      gap: 12px;
    }
  }
  @media (max-width: 480px) {
    .hero {
      min-height: 600px;
      padding-top: 40px;
    }
    .icon-wrapper {
      margin-bottom: 25px;
    }
    .icon-box {
      width: 95px;
      height: 90px;
    }
    .icon-inner img {
      width: 42px;
      height: 42px;
    }
    .planet {
      width: 850px;
      height: 420px;
      top: 50px;
    }
    .glow {
      width: 350px;
      height: 120px;
    }
    p {
      font-size: 13px;
    }
    .btn-outline,.btn-primary {
      width: 100%;
      max-width: 260px;
    }
  }
</style>
