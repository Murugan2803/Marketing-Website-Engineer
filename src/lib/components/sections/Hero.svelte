<script>
  import heroImage from "../../assets/Ai agent_img.png";
</script>

<section class="hero">
  <div class="wrapper">
    <div class="content">
      <div class="badge">
        <div class="badge-icon">
          <span class="star">✦</span>
        </div>
        <span class="text">Full Stack AI Agent Platform</span>
      </div>
      <h1>
        Ship the <span>agent.</span><br />
        Skip the <span>plumbing.</span>
      </h1>
      <p class="desc">
        Why are you still stitching together chat UIs, retries, moderation,
        notifications, and analytics — just to get your agent into users' hands?
      </p>
      <p class="desc">
        CometChat gives you the entire frontend + infra layer.<br/>
        Full stack. Modular. Production-ready.
      </p>
      <div class="buttons">
        <button class="outline">Schedule a Demo</button>
        <button class="primary">Try the Agent Builder</button>
      </div>
    </div>
    <div class="image">
      <img src={heroImage} alt="AI Agent UI" />
    </div>
  </div>
</section>

<style>
  .hero {
    width: 100%;
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: 20px 20px;
    color: white;
  }
  .wrapper {
    width: 100%;
    max-width: 1200px;
    margin: 10px 70px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 60px;
  }
  .content {
    padding-left: 10px;
    text-align: left;
  }
  .badge {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 6px 16px 6px 6px;
    border: 1px solid rgba(255, 255, 255, 0.25);
    border-radius: 999px;
    background: rgba(255, 255, 255, 0.03);
    backdrop-filter: blur(6px);
    color: #e6e6ff;
    font-size: 14px;
  }
  .badge-icon {
    width: 28px;
    height: 28px;
    border-radius: 50%;
    background: #f8f7fd;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .star {
    font-size: 14px;
    background: linear-gradient(180deg, #ad94f2 0%, #3302b8 160%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .text {
    line-height: 1;
  }
  .text {
    line-height: 1;
  }
  h1 {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 500;
    font-size: clamp(20px, 3vw, 36px);
    line-height: 1.1;
    margin-bottom: 25px;
    letter-spacing: 2px;
  }
  h1 span {
    background: linear-gradient(90deg, #a78bfa, #6366f1);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .desc {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 400;
    font-size: 20px;
    line-height: 1.2;
    color: #bdbdcf;
    margin-bottom: 15px;
    max-width: 520px;
  }
  .buttons {
    margin-top: 30px;
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
  }
  .primary {
    padding: 14px 26px;
    background: linear-gradient(90deg, #7c3aed, #6366f1);
    border: none;
    border-radius: 10px;
    color: white;
    font-weight: 600;
    cursor: pointer;
  }
  .outline {
    padding: 14px 26px;
    background: transparent;
    border: 1px solid #444;
    border-radius: 10px;
    color: white;
    font-weight: 600;
    cursor: pointer;
  }
  .image {
    display: flex;
    justify-content: flex-end;
  }
  .image img {
    width: 100%;
    max-width: 550px;
  }
  @media (max-width: 1200px){
    .content{
      padding-left: 10px;
    }
  }
  @media (max-width: 992px) {
    .wrapper {
      gap: 40px;
    }
    h1 {
      font-size: 44px;
    }
  }
  @media (max-width: 768px){
    .hero{
      padding: 60px 20px;
    }
    .wrapper{
      grid-template-columns: 1fr;
      margin: 0;
      gap: 30px;
      text-align: left;
    }
    .content{
      padding-left: 0;
      text-align: left;
    }
    h1{
      font-size: 32px;
      letter-spacing: 1px;
    }
    .desc{
      font-size: 16px;
      line-height: 1.5;
      margin-left: 0;
      margin-right: 0;
    }
    .buttons{
      justify-content: flex-start;
      flex-direction: column;
      width: 100%;
    }
    .buttons button{
      width: fit-content;
    }
    .image{
      justify-content: flex-start;
      margin-top: 20px;
    }
    .image img{
      max-width: 100%;
    }
  }
  @media (max-width: 480px){
    .badge{
      font-size: 12px;
      padding: 4px 12px 4px 4px;
    }
    h1{
      font-size: 26px;
      line-height: 1.2;
    }
    .desc{
      font-size: 14px;
    }
    .primary,
    .outline{
      padding: 12px 18px;
      font-size: 14px;
    }
  }
</style>
