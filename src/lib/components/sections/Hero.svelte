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
        CometChat gives you the entire frontend + infra layer. Full stack.
        Modular. Production-ready.
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
    padding: 80px 20px;
    color: white;
  }
  .wrapper {
    width: 100%;
    max-width: 1200px;
    margin: auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 60px;
  }
  .content {
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
    font-size: 50px;
    line-height: 1.1;
    margin-bottom: 25px;
  }
  h1 span {
    background: linear-gradient(90deg, #a78bfa, #6366f1);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .desc {
    font-size: 18px;
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
  @media (max-width: 992px) {
    .wrapper {
      gap: 40px;
    }
    h1 {
      font-size: 44px;
    }
  }
  @media (max-width: 768px) {
    .wrapper {
      grid-template-columns: 1fr;
      text-align: center;
    }
    .content {
      order: 1;
      text-align: center;
    }
    .image {
      order: 2;
      justify-content: center;
      margin-top: 40px;
    }
    .buttons {
      justify-content: center;
    }
    h1 {
      font-size: 36px;
    }
    .desc {
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>
