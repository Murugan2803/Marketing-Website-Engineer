<script>
  import imageUrl from "$lib/assets/Circle_img.png";
  const features = [
    "CometChat is the only full stack agent platform that combines logic, UI, moderation, notifications, and insights – without glue code.",
    "Each of these is battle-tested, used and trusted in production by real companies, across real user scenarios.",
  ];
</script>

<div class="left">
 <h2 class="title">
      Everything you’d end up <span class="gradient">already done.</span>
    </h2>
  <p class="subtitle">
    A complete frontend and system layer for AI agents. Plug in your LLM backend
    or build the brain with ours.
  </p>
  <ul class="feature-list">
    {#each features as feature}
      <li class="feature">
        <span class="icon">✦</span>
        <p>{feature}</p>
      </li>
    {/each}
  </ul>
</div>
<div class="right">
  <img src={imageUrl} alt="AI Agent Diagram" />
</div>

<style>
  .left {
    display: flex;
    flex-direction: column;
    gap: 24px;
  }
  .title {
    font-family: "Satoshi Variable", sans-serif;
    font-weight: 400;
    font-size: clamp(30px, 4vw, 48px);
  }
  .gradient {
    background: linear-gradient(90deg, #8b7cff, #6852d6);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .subtitle {
    font-size: clamp(16px, 1.6vw, 22px);
    opacity: 0.74;
  }
  .feature-list {
    list-style: none;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 18px;
  }
  .feature {
    display: flex;
    gap: 12px;
  }
  .icon {
    color: #6852d6;
  }
  .feature p {
    margin: 0;
    opacity: 0.74;
  }
  .right {
    display: flex;
    justify-content: center;
  }
  .right img {
    width: 100%;
    max-width: 480px;
  }
  @media (max-width: 768px) {
    .feature {
      justify-content: center;
    }
    .icon {
      display: none;
    }
  }
</style>
