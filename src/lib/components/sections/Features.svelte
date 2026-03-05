<section class="section">
  <div class="container">
    <div class="left-content">
      <div class="title-group">
        <h2 class="title">
          Everything your agent needs to go from prototype to product – fixed.
        </h2>
      </div>
      <p class="description">
        Modular when you want control. All-in-one when you just need to launch.
      </p>
    </div>
    <div class="features">
      {#each [
        ["Broken UI patterns", "Plug-and-play chat UI"],
        ["Duct-taped retries & feedback", "Robust, built-in feedback loops"],
        ["Manual guardrails", "Prebuilt safety net"],
        ["No alerts when things go wrong", "System alerts + observability"]
      ] as row}

      <div class="row">
        <div class="card bad">
          <span class="icon red">✕</span>
          {row[0]}
        </div>
        <div class="arrow">›››</div>
        <div class="card good">
          <span class="icon purple">✓</span>
          {row[1]}
        </div>
      </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .section {
    padding: clamp(70px, 10vw, 120px) 20px;
    background: #070712;
    color: white;
  }
  .container {
    max-width: 1200px;
    margin: auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: clamp(40px, 6vw, 80px);
    align-items: center;
  }
  .left-content {
    display: flex;
    flex-direction: column;
    gap: 18px;
    max-width: 520px;
  }
  .title {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 400;
    font-size: clamp(28px, 4vw, 46px);
    line-height: 1.1;
    color: #fafaff;
  }
  .description {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 500;
    font-size: clamp(15px, 2vw, 22px);
    line-height: 1.4;
    color: #fafaff;
    opacity: 0.74;
  }
  .features {
    display: flex;
    flex-direction: column;
    gap: clamp(14px, 2vw, 22px);
  }
  .row {
    display: flex;
    align-items: center;
    gap: clamp(10px, 1.5vw, 16px);
    flex-wrap: nowrap;
    position: relative;
  }
  .row::before {
    content: "";
    position: absolute;
    left: 35%;
    right: 35%;
    height: 80px;
    background: radial-gradient(
      circle,
      rgba(139,124,255,0.45) 0%,
      rgba(139,124,255,0.18) 35%,
      rgba(139,124,255,0.05) 60%,
      transparent 80%
    );
    filter: blur(40px);
    z-index: 0;
  }
  .card {
    padding: clamp(12px, 1.2vw, 16px) clamp(14px, 1.5vw, 20px);
    border-radius: 14px;
    background: #0d0f1a;
    border: 1px solid rgba(255, 255, 255, 0.06);
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: clamp(13px, 1vw, 15px);
    flex: 1;
    min-width: 0;
    position: relative;
    z-index: 2;
  }
  .bad {
    color: #d1d5db;
  }
  .good {
    color: #e5e7ff;
    border: 1px solid rgba(139,124,255,0.4);
    background: #0d0f1a;
    box-shadow:
      -18px 0 28px -10px rgba(139,124,255,0.45),
      18px 0 28px -10px rgba(139,124,255,0.45);
  }
  .icon {
    font-weight: bold;
  }
  .red {
    color: #ff5a5a;
  }
  .purple {
    color: #8b7cff;
    text-shadow:
      0 0 6px rgba(139,124,255,0.8),
      0 0 12px rgba(139,124,255,0.6);
  }
  .arrow {
    color: #8b7cff;
    font-size: clamp(16px, 1.4vw, 18px);
    letter-spacing: 4px;
    position: relative;
    z-index: 2;
    text-shadow:
      0 0 6px rgba(139,124,255,0.8),
      0 0 16px rgba(139,124,255,0.6),
      0 0 30px rgba(139,124,255,0.4);
  }
  @media (max-width: 1024px) {
    .container {
      grid-template-columns: 1fr;
      gap: 60px;
    }
    .left-content {
      max-width: 100%;
    }
  }
  @media (max-width: 768px) {
    .row {
      flex-direction: column;
      align-items: stretch;
    }
    .arrow {
      display: none;
    }
    .card {
      width: 100%;
    }
  }
  @media (max-width: 480px) {
    .section {
      padding: 60px 16px;
    }
    .title {
      font-size: 26px;
    }
    .description {
      font-size: 15px;
    }
  }
</style>