<script>
  import heroImage from "../../assets/Ai agent_img.png";
</script>

<section class="hero">
  <div class="wrapper">

    <!-- LEFT CONTENT -->
    <div class="content">
      <div class="badge">
        ✨ Full Stack AI Agent Platform
      </div>

      <h1>
        Ship the <span>agent.</span><br />
        Skip the <span>plumbing.</span>
      </h1>

      <p class="desc">
        Why are you still stitching together chat UIs, retries,
        moderation, notifications, and analytics — just to get
        your agent into users' hands?
      </p>

      <p class="desc">
        CometChat gives you the entire frontend + infra layer.
        Full stack. Modular. Production-ready.
      </p>

      <div class="buttons">
        <button class="outline">Schedule a Demo</button>
        <button class="primary">Try the Agent Builder</button>
      </div>
    </div>

    <!-- RIGHT IMAGE -->
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
    background: radial-gradient(circle at 70% 30%, #1a1443, #0b0b1f 60%);
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

  /* LEFT */
  .content {
    text-align: left;
  }

  .badge {
    display: inline-block;
    padding: 8px 16px;
    background: rgba(255, 255, 255, 0.08);
    border-radius: 50px;
    font-size: 14px;
    margin-bottom: 25px;
  }

  h1 {
    font-size: 56px;
    line-height: 1.1;
    margin-bottom: 25px;
    font-weight: 700;
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

  /* RIGHT */
  .image {
    display: flex;
    justify-content: flex-end;
  }

  .image img {
    width: 100%;
    max-width: 450px;
    border-radius: 20px;
    box-shadow: 0 0 60px rgba(124, 58, 237, 0.4);
  }

  /* ------------------ RESPONSIVE ------------------ */

  /* Tablet */
  @media (max-width: 992px) {
    .wrapper {
      gap: 40px;
    }

    h1 {
      font-size: 44px;
    }
  }

  /* Mobile */
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