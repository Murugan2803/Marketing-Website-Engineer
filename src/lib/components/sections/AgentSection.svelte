<script>
    const cards = [
        {
            title: "Chat Builder",
            desc: "The fastest way to go live.",
            link: "Try Builder",
            icon: "⚙️",
            features: [
                "Visual interface for styling and configuring chat",
                "Drop into any web or mobile app with a single snippet",
                "Integrates with auth, analytics, and third-party tools",
                "Great for prototypes, pilots, or teams with limited frontend resources",
            ],
        },
        {
            title: "UI Kits",
            desc: "Production-ready components with full flexibility.",
            link: "Try Builder",
            icon: "✨",
            features: [
                "Available for all popular frameworks",
                "Theming, layout, and logic hooks exposed",
                "Save time on structure, focus on experience",
                "Ideal for teams who want speed and polish",
            ],
        },
        {
            title: "SDKs & APIs",
            desc: "The toolbox for when you want total control.",
            link: "Try Builder",
            icon: "⚛️",
            features: [
                "Available for all popular frameworks",
                "Theming, layout, and logic hooks exposed",
                "Save time on structure, focus on experience",
                "Ideal for teams who want speed and polish",
            ],
        },
    ];
</script>

<section class="section">
    <div class="heading">
        <p class="tag">Chat integration options</p>

        <h1 class="title">Your launch, your way. Done right.</h1>

        <p class="sub">
            Start with what gets you to production fastest — or matches your
            needs the best.<br />
            Swap it out or level it up later.
        </p>
    </div>

    <!-- TOP GRID LINE -->
    <div class="grid-line top"></div>

    <div class="cards">
        {#each cards as card}
            <div class="card">
                <div class="icon">{card.icon}</div>

                <h3>{card.title}</h3>

                <p class="desc">{card.desc}</p>

                <ul class="features">
                    {#each card.features as feature}
                        <li>✦ {feature}</li>
                    {/each}
                </ul>

                <a href="#">{card.link}</a>
            </div>
        {/each}
    </div>

    <!-- BOTTOM GRID LINE -->
    <div class="grid-line bottom"></div>
</section>

<style>
    .section {
        background: #050510;
        padding: clamp(20px, 8vw, 50px) 6%;
        color: white;
        text-align: center;
    }

    /* TEXT */

    .tag {
        font-family: "Satoshi Variable", sans-serif;
        font-size: clamp(16px, 2vw, 22px);
        color: #6852d6;
    }

    .title {
        font-family: "Satoshi Variable", sans-serif;
        font-size: clamp(24px, 4vw, 36px);
        color: #fafaff;
        margin-top: 10px;
    }

    .sub {
        font-family: "Satoshi Variable", sans-serif;
        font-size: clamp(14px, 1.5vw, 16px);
        color: #fafaff;
        opacity: 0.74;
        margin-top: 10px;
    }

    /* GRID LINES */

    .grid-line {
        width: 100%;
        height: 1px;
        background: rgba(255, 255, 255, 0.1);
        margin: 40px 0;
    }

    /* CARDS GRID */

    .cards {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 30px;
        max-width: 1200px;
        margin: auto;
    }

    /* TABLET */

    @media (max-width: 1024px) {
        .cards {
            grid-template-columns: repeat(2, 1fr);
        }
    }

    /* MOBILE */

    @media (max-width: 640px) {
        .cards {
            grid-template-columns: 1fr;
        }

        .grid-line {
            display: none;
        }
    }

    /* CARD */

    .card {
        position: relative;
        padding: 40px 30px;
        border-radius: 14px;
        background: rgba(20, 20, 40, 0.6);
        border: 1px solid rgba(255, 255, 255, 0.05);
        text-align: left;
        transition: 0.35s ease;
        overflow: hidden;
    }

    /* ICON */

    .icon {
        width: 48px;
        height: 48px;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 12px;
        border: 1px solid rgba(255, 255, 255, 0.08);
        background: #0f0f1f;
        margin-bottom: 20px;
        font-size: 20px;
    }

    /* GLOW EFFECT */

    .card::before {
        content: "";
        position: absolute;
        inset: 0;
        background: radial-gradient(
            circle at center,
            rgba(120, 80, 255, 0.35),
            transparent 70%
        );
        opacity: 0;
        transition: 0.35s;
        filter: blur(40px);
    }

    .card:hover::before {
        opacity: 1;
    }

    .card:hover {
        transform: translateY(-6px) scale(1.02);
        border-color: rgba(130, 100, 255, 0.4);
    }

    /* TEXT */

    h3 {
        margin-bottom: 14px;
        font-size: 20px;
    }

    .desc {
        color: #9aa0b3;
        transition: 0.3s;
    }

    /* FEATURES */

    .features {
        list-style: none;
        padding: 0;
        margin-top: 10px;
        opacity: 0;
        max-height: 0;
        overflow: hidden;
        transition: 0.35s;
        color: #c7c7e8;
        font-size: 14px;
        line-height: 1.6;
    }

    .features li {
        margin-bottom: 6px;
    }

    /* HOVER CONTENT CHANGE */

    .card:hover .desc {
        opacity: 0;
        max-height: 0;
    }

    .card:hover .features {
        opacity: 1;
        max-height: 300px;
    }

    /* LINK */

    a {
        display: inline-block;
        margin-top: 20px;
        color: #7a6cff;
        font-size: 14px;
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }
</style>
