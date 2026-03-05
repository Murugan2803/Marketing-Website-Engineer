<script lang="ts">
    let isOpen: boolean = false;
    let active: string = "Platform";
    interface NavLink {
        label: string;
        href: string;
    }
    const links: NavLink[] = [
        { label: "Platform", href: "#" },
        { label: "Solutions", href: "#" },
        { label: "Developers", href: "#" },
        { label: "Resources", href: "#" },
        { label: "Pricing", href: "#" },
    ];
    function handleClick(label: string): void {
        active = label;
        isOpen = false;
    }
</script>

<header class="navbar">
    <div class="container">
        <a href="/" class="logo">comet<b>chat</b></a>
        <nav class="nav">
            {#each links as link}
                <a
                    href={link.href}
                    class:active={active === link.label}
                    on:click={() => handleClick(link.label)}
                >
                    {link.label}
                </a>
            {/each}
        </nav>
        <div class="actions">
            <a href="#" class="login">Log in</a>
            <a href="#" class="cta">Schedule a demo</a>
        </div>
        <button
            class="menu-toggle"
            aria-label="Toggle menu"
            on:click={() => (isOpen = !isOpen)}
        >
            ☰
        </button>
    </div>
    {#if isOpen}
        <div class="mobile-menu">
            {#each links as link}
                <a
                    href={link.href}
                    class:active={active === link.label}
                    on:click={() => handleClick(link.label)}
                >
                    {link.label}
                </a>
            {/each}
            <a href="#" class="login">Log in</a>
            <a href="#" class="cta">Schedule a demo</a>
        </div>
    {/if}
</header>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap");
    .navbar {
        background: #07071c;
        width: 100%;
        position: sticky;
        top: 0;
        z-index: 1000;
    }
    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 18px 24px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .logo {
        font-family: "Inter", sans-serif;
        font-size: 18px;
        color: #ffffff;
        text-decoration: none;
        letter-spacing: -0.2px;
    }
    .nav {
        display: flex;
        gap: 36px;
    }
    .nav a {
        font-family: "Inter", sans-serif;
        font-size: 12.5px;
        font-weight: 400;
        color: #b8b8c7;
        text-decoration: none;
        transition: color 0.2s ease;
    }
    .nav a:hover {
        color: #ffffff;
    }
    .nav a.active,
    .mobile-menu a.active {
        color: rgb(140, 124, 224);
        font-weight: 400;
    }
    .actions {
        display: flex;
        align-items: center;
        gap: 22px;
    }
    .login {
        font-family: "Inter", sans-serif;
        font-size: 12.5px;
        color: #b8b8c7;
        text-decoration: none;
    }
    .login:hover {
        color: #ffffff;
    }
    .cta {
        font-family: "Inter", sans-serif;
        font-size: 12px;
        font-weight: 500;
        padding: 9px 18px;
        border-radius: 999px;
        text-decoration: none;
        color: white;
        background: linear-gradient(135deg, #7b61ff 0%, #5a3df0 100%);
        box-shadow: 0 0 20px rgba(123, 97, 255, 0.25);
        transition:
            transform 0.15s ease,
            box-shadow 0.15s ease;
    }
    .cta:hover {
        transform: translateY(-1px);
        box-shadow: 0 6px 24px rgba(123, 97, 255, 0.4);
    }
    .menu-toggle {
        display: none;
        font-size: 22px;
        background: none;
        border: none;
        color: white;
        cursor: pointer;
    }
    .mobile-menu {
        display: flex;
        flex-direction: column;
        gap: 16px;
        padding: 20px 24px;
        background: #0d0d26;
    }
    @media (max-width: 900px) {
        .nav,
        .actions {
            display: none;
        }

        .menu-toggle {
            display: block;
        }
    }
</style>
