<script>
    import Button from "../Button.svelte";
import List from "./List.svelte";


</script>

<div class="footer">
    <div class="lists">
        <List title=Products points={["Why Achained?", "Achained updates", "Credential Hub", "Institution profile", "Achained Blockchain", "Security", "Network status"]} />
        <List title=Resources points={["Achained tutorial", "Creating credentials", "Accepting credentials", "Third party implementations"]} />
        <List title=Community points={["Blog", "Our Team", "Careers", "The history", "Events"]} />
        <List title=Help points={["Contact", "Speak to Sales", "Privacy Policy", "Terms of Service", "Trademark Policy", "Inactivity Policy", "Support Terms", "Cookie Preferences"]} />
    </div>
    <div class="info">
        <img src="logo.png" alt="Achained" class="logo">
        <div class="socials">
            <a href="index.html"><img src="twitter.png" alt="Twitter"></a>
            <a href="index.html" class="insta"><img src="instagram.png" alt="Instagram"></a>
            <a href="index.html"><img src="linkedin2.png" alt="LinkedIn"></a>
        </div>
        <div class="but">
            <Button content="Join the network" type="primary"/>
        </div>
        <span>© 2022 All Rights Reseved. Achained Inc.</span>
    </div>
</div>

<style>

    span {
        font-size: 10px;
        font-weight: 400;
    }

    .footer {
        background-color: var(--bkg);
        width: 100%;
        height: 500px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .lists {
        width: 895px;
        display: flex;
        justify-content: space-between;
    }

    .info {
        margin-left: 149px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .logo {
        width: 116px;
        height: 24.18px;
        margin-top: 10px;
    }

    .socials {
        margin-top: 22px;
        margin-bottom: 47px;
    }

    .socials img {
        width: 20px;
        height: 20px;
    }

    .insta {
        margin: 0 14px 0 14px;
    }

    .but {
        margin-bottom: 96px;
    }
</style>