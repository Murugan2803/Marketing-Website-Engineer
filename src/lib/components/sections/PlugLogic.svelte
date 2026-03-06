<script>
  import imageURL from "../../assets/twilio_img.png";
  const features = [
    "Native push, email, and SMS support",
    "Retry logic, delivery throttling, and batching",
    "Trigger-based delivery rules - unread X mins, fallback triggered, user went silent",
    "Threaded email replies (yes, replies go back to chat!)",
    "Integrates with SendGrid, Twilio, or your custom providers",
    "User-level frequency + preference settings",
  ];
</script>

<section class="hero">
  <div class="container">
    <div class="left">
      <p class="label">Multichannel notifications engine</p>
      <h2 class="title">
        Your agent is only helpful if people <br /> come back to talk to it.
      </h2>
      <p class="desc">Most agents get ghosted. Yours won’t.</p>
      <ul class="features">
        {#each features as item}
          <li>
            <span class="icon">✦</span>
            <span>{item}</span>
          </li>
        {/each}
      </ul>
      <p class="footer">
        Notifications aren’t a growth hack. They’re UX glue. And we built them<br
        />
        so you wouldn’t have to.
      </p>
    </div>
    <div class="right">
      <img src={imageURL} alt="notification system" />
    </div>
  </div>
</section>

<style>
  .hero {
    background: #070614;
    padding: clamp(60px, 8vw, 100px) 6%;
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
