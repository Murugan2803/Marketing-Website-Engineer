<script>
  import imageURL from "../../assets/chart_img.png";
  const features = [
    "Resolution rates, fallback frequency, retry counts, latency",
    "Tool usage breakdowns, prompt paths, knowledge base hits",
    "Conversation-level analytics: drop-off points, re-engagement, success outcomes",
    "Sentiment markers and feedback loops",
    "Exportable, filterable, and privacy-respectful",
  ];
</script>

<section class="hero">
  <div class="container">
    <div class="left">
      <div class="title-group">
        <p class="label">Insights dashboard</p>
        <h2 class="title">
          Ship the agent. Then make it better. Without needing Mixpanel,
          Segment, or BI setups.
        </h2>
      </div>
      <p class="desc">
        From day one, you get built-in visibility into what your agent is doing
        – and how people are responding.
      </p>
      <ul class="features">
        {#each features as item}
          <li>
            <span class="icon">✦</span>
            <span>{item}</span>
          </li>
        {/each}
      </ul>
      <p class="footer">
        You can’t improve what you can’t see. With us, you never ship blind.
      </p>
    </div>
    <div class="right">
      <img src={imageURL} alt="Insights dashboard" />
    </div>
  </div>
</section>

<style>
  .hero {
    background: #070614;
    padding: clamp(40px, 8vw, 70px) 6%;
    color: white;
  }
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 16px;
    display: grid;
    grid-template-columns: minmax(220px, 588px) 1fr;
    gap: 80px;
    align-items: center;
  }
  .left {
    flex: 1;
    max-width: 600px;
    display: flex;
    flex-direction: column;
    gap: 16px;
  }
  .title-group {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
  .label {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 400;
    font-size: clamp(16px, 2vw, 22px);
    line-height: 106%;
    color: #6852d6;
    margin: 0;
  }
  .title {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 400;
    font-size: clamp(20px, 3vw, 26px);
    line-height: 110%;
    color: #fafaff;
    margin: 0;
  }
  .desc {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 400;
    font-size: clamp(14px, 1.6vw, 16px);
    line-height: 120%;
    letter-spacing: 0.005em;
    color: #fafaff;
    opacity: 0.74;
    margin: 0;
  }
  .features {
    display: flex;
    flex-direction: column;
    gap: 12px;
    padding: 0;
    margin: 10px 0;
    list-style: none;
  }
  .features li {
    display: flex;
    gap: 8px;
    align-items: flex-start;
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 400;
    font-size: clamp(13px, 1.4vw, 16px);
    line-height: 130%;
    letter-spacing: 0.005em;
    color: #fafaff;
    opacity: 0.74;
  }
  .icon {
    color: #6852d6;
    font-size: 16px;
    margin-top: 3px;
  }
  .footer {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 400;
    font-size: clamp(13px, 1.4vw, 14px);
    line-height: 140%;
    letter-spacing: 0.005em;
    color: #fafaff;
    opacity: 0.74;
    margin-top: 6px;
  }
  .right {
    flex: 1;
    display: flex;
    justify-content: center;
  }
  .right img {
    width: 100%;
    max-width: 520px;
    height: auto;
  }
  @media (max-width: 1100px) {
    .container {
      grid-template-columns: minmax(120px, 328px) 1fr;
      gap: 80px;
    }
    .title {
      font-size: 18px;
      line-height: 1.2;
    }
    .desc {
      font-size: 16px;
    }
    .features li {
      justify-content: flex-start;
      text-align: left;
      font-size: 14px;
    }
  }
  @media (max-width: 900px) {
    .hero {
      padding: 70px 20px;
    }
    .container {
      grid-template-columns: 1fr;
      gap: 48px;
    }
    .left {
      align-items: flex-start;
      text-align: left;
      max-width: 100%;
    }
    .title {
      font-size: 20px;
      line-height: 1.2;
    }
    .desc {
      font-size: 16px;
    }
    .features li {
      justify-content: flex-start;
      text-align: left;
    }
  }
  @media (max-width: 500px) {
    .hero {
      padding: 0px;
    }
    .features li {
      font-size: 14px;
    }
  }
</style>
