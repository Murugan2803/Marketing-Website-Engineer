<script>
    import imageURLComet from "../../assets/CometChat Logo.png";
    import facebook from "../../assets/icon/facebook.png";
    import linkedin from "../../assets/icon/linkedin.png";
    import instagram from "../../assets/icon/instagram.png";
    import twitter from "../../assets/icon/twitter.png";
    import github from "../../assets/icon/github.png";
    const columns = [
        {
            title: "Platform",
            links: [
                { name: "Chat & Messaging" },
                { name: "Voice & Video Calls" },
                { name: "Features", muted: true },
                { name: "Chat & Messaging" },
                { name: "Voice & Video Calls" },
                { name: "Notifications" },
                { name: "Analytics & Insights" },
                { name: "Multi-Tenant Chat" },
                { name: "Integration Methods" },
                { name: "UI Kits" },
                { name: "SDKs & APIs" },
            ],
        },
        {
            title: "Solutions",
            links: [
                { name: "By Use cases" },
                { name: "On-demand" },
                { name: "Online Marketplaces" },
                { name: "SaaS Businesses" },
                { name: "Healthcare & Telehealth" },
                { name: "Community & Social" },
                { name: "Dating" },
                { name: "Comparison", muted: true },
                { name: "CometChat vs Sendbird" },
                { name: "Compare Top Chat SDKs" },
                { name: "Sendbird Alternatives" },
                { name: "Stream Chat Alternatives" },
            ],
        },
        {
            title: "Developers",
            links: [
                { name: "Docs" },
                { name: "Sample Apps" },
                { name: "APIs" },
                { name: "Product Updates" },
                { name: "Feature Requests" },
                { name: "System Status" },
                { name: "Support", muted: true },
                { name: "Community" },
                { name: "Help Center" },
                { name: "Office Hours" },
                { name: "Report an issue" },
            ],
        },
        {
            title: "Resources",
            links: [
                { name: "Templates" },
                { name: "Tutorials" },
                { name: "Blog" },
                { name: "Chat UI Kits", muted: true },
                { name: "React Chat UI Kit" },
                { name: "Flutter Chat UI Kit" },
                { name: "Android Chat UI Kit" },
                { name: "React Native Chat UI Kit" },
                { name: "iOS Chat UI Kit" },
            ],
        },
        {
            title: "Company",
            links: [
                { name: "Careers" },
                { name: "Partners" },
                { name: "Pricing" },
                { name: "Implementation Services" },
                { name: "Chat with us" },
                { name: "Terms and Legal", muted: true },
                { name: "Terms of Service" },
                { name: "Privacy Policy" },
                { name: "Sub-processors List" },
                { name: "Data Processing Addendum" },
                { name: "Vulnerability Disclosure Program" },
            ],
        },
    ];
</script>

<footer class="footer">
    <div class="container">
        <div class="top-logo">
            <a href="/" class="side-logo">comet<b>chat</b></a>
        </div>
        <div class="grid">
            {#each columns as col}
                <div class="col">
                    <h3>{col.title}</h3>
                    <ul>
                        {#each col.links as link}
                            <li class:muted={link.muted}>
                                {link.name}
                            </li>
                        {/each}
                    </ul>
                </div>
            {/each}
        </div>
        <div class="logo">
            <img src={imageURLComet} alt="logo" />
        </div>
        <div class="bottom">
            <div class="copyright">
                © 2025 CometChat
                <span>Terms of Use</span>
                <span>Privacy Policy</span>
            </div>
            <div class="social">
                <div class="social-item">
                    <img src={facebook} alt="facebook" />
                    <span>Facebook</span>
                </div>
                <div class="social-item">
                    <img src={linkedin} alt="linkedin" />
                    <span>LinkedIn</span>
                </div>
                <div class="social-item">
                    <img src={instagram} alt="instagram" />
                    <span>Instagram</span>
                </div>
                <div class="social-item">
                    <img src={twitter} alt="twitter" />
                    <span>Twitter</span>
                </div>
                <div class="social-item">
                    <img src={github} alt="github" />
                    <span>GitHub</span>
                </div>
            </div>
        </div>
    </div>
</footer>

<style>
    .footer {
        background: #070614;
        position: relative;
        color: #b8b9d6;
        padding: 70px 40px 30px;
        overflow: hidden;
        font-family: Inter, sans-serif;
    }
    .container {
        max-width: 1400px;
        margin: auto;
    }
    .top-logo {
        margin-bottom: 40px;
    }
    .side-logo {
        font-size: 28px;
        color: #fff;
        text-decoration: none;
    }
    .logo {
        display: flex;
        justify-content: center;
    }
    .logo img {
        width: 90%;
        margin: 40px 0;
    }
    .grid {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        gap: 40px;
    }
    h3 {
        color: #7c7cff;
        font-size: 16px;
        margin-bottom: 14px;
    }
    ul {
        list-style: none;
        padding: 0;
    }
    li {
        font-size: 14px;
        margin-bottom: 10px;
        cursor: pointer;
        transition: 0.2s;
    }
    li:hover {
        color: #fff;
    }
    li.muted {
        color: #6b6d85;
        margin-top: 18px;
        cursor: default;
    }
    .bottom {
        border-top: 1px solid rgba(255, 255, 255, 0.08);
        margin-top: 50px;
        padding-top: 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .copyright span {
        margin-left: 20px;
        cursor: pointer;
    }
    .social {
        display: flex;
        gap: 20px;
    }
    .social-item {
        display: flex;
        align-items: center;
        gap: 6px;
        cursor: pointer;
        opacity: 0.8;
        font-size: 14px;
    }
    .social-item img {
        width: 16px;
    }
    .social-item:hover {
        opacity: 1;
    }
    @media (max-width: 1024px) {
        .grid {
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }
        .footer {
            padding: 60px 30px 30px;
        }
    }
    @media (max-width: 768px) {
        .grid {
            grid-template-columns: repeat(2, 1fr);
            gap: 25px;
        }
        .logo img {
            width: 100%;
        }
        .bottom {
            flex-direction: column;
            align-items: flex-start;
            gap: 15px;
        }
        .social {
            flex-wrap: wrap;
        }
    }
    @media (max-width: 480px) {
        .footer {
            padding: 50px 20px 20px;
        }
        .grid {
            grid-template-columns: 1fr;
            gap: 25px;
        }
        .top-logo {
            text-align: left;
        }
        .logo {
            justify-content: flex-start;
        }
        .logo img {
            width: 100%;
        }
        .bottom {
            align-items: flex-start;
        }
        .copyright span {
            display: block;
            margin-left: 0;
            margin-top: 5px;
        }
        .social {
            gap: 15px;
        }
    }
</style>
