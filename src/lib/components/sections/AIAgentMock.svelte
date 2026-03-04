<script>
  let message = "";

  const actions = [
    "Create image",
    "Analyze data",
    "Make a plan",
    "Summarize text",
    "Help me write",
    "More"
  ];
</script>

<section class="wrapper">
  <div class="grid"></div>

  <!-- CONNECTOR LINES -->
  <div class="line left-top"></div>
  <div class="line right-top"></div>
  <div class="line right-mid"></div>
  <div class="line left-bottom"></div>

  <!-- FLOATING LABELS -->
  <div class="label l1">✦ UI Kits</div>
  <div class="label l2">✂ Moderation</div>
  <div class="label l3">📊 Analytics</div>
  <div class="label l4">🔔 Notification</div>

  <!-- CARD -->
  <div class="card">
    <div class="header">
      <div class="left">
        <div class="mini-icon">✦</div>
        <span class="agent-text">AI Agent</span>
      </div>
      <div class="right">
        <span>＋</span>
        <span>↻</span>
      </div>
    </div>

    <div class="content">
      <div class="avatar">✦</div>
      <p class="hello">Hello, Jack!</p>
      <h2>How can I help?</h2>

      <div class="actions">
        {#each actions as action}
          <button>{action} →</button>
        {/each}
      </div>
    </div>

    <div class="input">
      <input bind:value={message} placeholder="Ask anything..." />
      <div class="icons">
        <span>＋</span>
        <span>🎤</span>
        <button>↑</button>
      </div>
    </div>
  </div>
</section>

<style>
  :global(body) {
    margin: 0;
    background: #050317;
    font-family: Inter, system-ui, sans-serif;
    color: white;
  }

  .wrapper {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
  }

  /* Subtle Grid */
  .grid {
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(rgba(255,255,255,0.035) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.035) 1px, transparent 1px);
    background-size: 40px 40px;
    opacity: 0.2;
  }

  /* CARD */
  .card {
    width: 360px;
    padding: 22px;
    border-radius: 30px;
    background: linear-gradient(180deg, #16142f 0%, #0d0b1f 100%);
    position: relative;
    box-shadow: 0 0 70px rgba(124,92,255,0.25);
  }

  .card::before {
    content: "";
    position: absolute;
    inset: -2px;
    border-radius: 32px;
    background: linear-gradient(
      45deg,
      #00e0ff,
      #7c5cff,
      #ff5c9d,
      #00ffb3
    );
    z-index: -1;
    filter: blur(18px);
    opacity: 0.65;
  }

  /* HEADER */
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 14px;
  }

  .left {
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .mini-icon {
    width: 24px;
    height: 24px;
    border-radius: 50%;
    background: linear-gradient(45deg, #00e0ff, #7c5cff);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 11px;
  }

  .agent-text {
    font-weight: 500;
    color: #ddd;
  }

  .right span {
    margin-left: 12px;
    cursor: pointer;
    opacity: 0.7;
  }

  /* CONTENT */
  .content {
    text-align: center;
    margin-top: 32px;
  }

  .avatar {
    width: 60px;
    height: 60px;
    margin: 0 auto 14px;
    border-radius: 50%;
    background: linear-gradient(45deg, #7c5cff, #00e0ff);
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .hello {
    opacity: 0.55;
    font-size: 14px;
    margin: 4px 0;
  }

  h2 {
    margin: 6px 0 22px;
    font-weight: 500;
    letter-spacing: -0.3px;
  }

  /* ACTION BUTTONS */
  .actions {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
  }

  .actions button {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.08);
    padding: 6px 14px;
    border-radius: 999px;
    font-size: 12.5px;
    color: #e6e6e6;
    cursor: pointer;
  }

  .actions button:hover {
    background: rgba(124,92,255,0.25);
  }

  /* INPUT */
  .input {
    margin-top: 26px;
    background: rgba(255,255,255,0.05);
    padding: 8px 12px;
    border-radius: 999px;
    display: flex;
    align-items: center;
  }

  input {
    flex: 1;
    background: transparent;
    border: none;
    color: white;
    outline: none;
    font-size: 13px;
  }

  .icons {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .icons button {
    width: 28px;
    height: 28px;
    border-radius: 50%;
    border: none;
    background: #222;
    color: white;
    cursor: pointer;
  }

  /* FLOATING LABELS */
  .label {
    position: absolute;
    padding: 8px 14px;
    background: rgba(255,255,255,0.05);
    border-radius: 14px;
    backdrop-filter: blur(10px);
    font-size: 13px;
    color: #d8d8d8;
  }

  .l1 { left: 18%; top: 38%; }
  .l2 { right: 18%; top: 30%; }
  .l3 { right: 18%; bottom: 36%; }
  .l4 { left: 18%; bottom: 30%; }

  /* CONNECTOR LINES */
  .line {
    position: absolute;
    width: 120px;
    height: 1px;
    background: linear-gradient(90deg, transparent, #7c5cff, transparent);
    opacity: 0.4;
  }

  .left-top { left: 28%; top: 40%; transform: rotate(-30deg); }
  .right-top { right: 28%; top: 32%; transform: rotate(30deg); }
  .right-mid { right: 28%; bottom: 38%; transform: rotate(-20deg); }
  .left-bottom { left: 28%; bottom: 32%; transform: rotate(25deg); }

  /* RESPONSIVE */
  @media (max-width: 900px) {
    .label, .line {
      display: none;
    }
  }

  @media (max-width: 480px) {
    .card {
      width: 92%;
    }
  }
</style>