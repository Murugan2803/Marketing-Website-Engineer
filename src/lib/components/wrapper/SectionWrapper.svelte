<section class="section">
    <div class="container">
        <slot></slot>
    </div>
</section>

<style>
    .section {
        /* padding: 50px 24px; */
        background: #070712;
        color: #fafaff;
    }
    .container {
        max-width: 1200px;
        margin: auto;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 80px;
        align-items: center;
    }
    @media (max-width: 768px) {
        .container {
            grid-template-columns: 1fr;
            text-align: left;
        }
    }
</style>
