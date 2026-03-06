<script>
    import imageURL from "../../assets/Phn_AI_agent_img.png";
    const features = [
        "Token streaming with dynamic 'thinking...' states",
        "Retry/stop buttons with full control logic",
        "Memory pills, prompt banners, and agent selectors",
        "Structured tool replies with inline citations",
        "Slash commands, modals, and frontend triggers",
        "Low/No-code Chat Builder, or more control via UI Kits and SDKs",
        "Fully AG-UI protocol compatible — including tool call rendering, memory markers, and fallback patterns",
    ];
</script>

<section class="hero">
    <div class="container">
        <div class="left">
            <p class="tag">Production-ready chat UI</p>
            <h3 class="title">
                The UX layer your agent deserves.<br />
                Built for LLM-native interactions,<br />
                out of the box.
            </h3>
            <p class="desc">
                Forget cobbling together buttons and hoping users ‘get it’. Our
                chat layer is purpose-built for how agents think — and how
                humans expect them to respond.
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
                It’s not just a pretty shell. It’s UX that teaches trust, guides
                behavior, and makes your agent feel alive.
            </p>
        </div>
        <div class="image">
            <img src={imageURL} alt="AI Agent UI" />
        </div>
    </div>
</section>

<style>
    .hero {
       background: #070614;
        padding: 80px 40px;
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
        display: flex;
        flex-direction: column;
        gap: 16px;
        width: 100%;
    }
    .tag {
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
    .image {
        display: flex;
        justify-content: center;
        width: 100%;
    }
    .image img {
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




