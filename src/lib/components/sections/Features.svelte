<section class="section">
  <div class="container grid-2">

    <div>
      <h2>
        Everything your agent needs to go from prototype to product — fixed.
      </h2>
      <p>
        Modular when you want control. All-in-one when you need to launch.
      </p>
    </div>

    <div class="cards">
      {#each [
        "Broken UI patterns",
        "Plugin-and-play chat UI",
        "Manual guardrails",
        "Privacy safety net",
        "System alerts + observability"
      ] as item}
        <div class="card">{item}</div>
      {/each}
    </div>

  </div>
</section>

<style>
.cards {
  display: grid;
  gap: var(--space-3);
}

.card {
  background: var(--bg-secondary);
  padding: var(--space-3);
  border-radius: 14px;
}
</style>