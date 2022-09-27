<script>
    import Bullets from "./Bullets.svelte";
    import Slider from "./Slider.svelte";

    let show;
</script>

<div class="intro">
    <div class="container">
        <div class="slider">
            <Slider bind:current={show}/>
        </div>
        {#if show === 'right'}
            <div class="content">
                <div class="text">
                    <h4>Why Achained?</h4>
                    <h2>Make your work worth</h2>
                    <div class="first">
                        <Bullets title="For your education:" explain="Make your diplomas instantly verifiable"/>
                    </div>
                    <div class="second">
                        <Bullets title="For your experience:" explain="Claim the authenticity of your work experience"/>
                    </div>
                    <div class="third">
                        <Bullets title="For your skills:" explain="Convert your abilities to personal assets"/>
                    </div>
                </div>
                <div class="picture">
                    <img src="carpenter.jpg" alt="Carpenter">
                    <a href="index.html">
                        <h3>Try it now</h3>
                        <img src="arrow.png" alt="Arrow" class="try">
                    </a>
                </div>
            </div>
        {:else}
            <div class="content">
                <div class="text">
                    <h4>Why Achained?</h4>
                    <h2>Take the credit you deserve</h2>
                    <div class="first">
                        <Bullets title="For your students:" explain="Create a secure and verifiable progress"/>
                    </div>
                    <div class="second">
                        <Bullets title="For your alumni:" explain="Let them show odd where they studied"/>
                    </div>
                    <div class="third">
                        <Bullets title="For your institution:" explain="Keep your reputation spotless"/>
                    </div>
                </div>
                <div class="picture">
                    <img src="classroom.jpg" alt="Carpenter">
                    <a href="index.html">
                        <h3>Try it now</h3>
                        <img src="arrow.png" alt="Arrow" class="try">
                    </a>
                </div>
            </div>
        {/if}
    </div>
</div>

<style>
    a {
        background-color: var(--primary-color);
        color: #1e1e1e;
        text-decoration: none;
        width: 167px;
        height: 49px;
        border: 2px solid #1e1e1e;
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        left: 210px;
        top: 201px;
        transition: box-shadow 0.2s linear 0s;
    }

    a:hover {
        box-shadow: inset 167px 0 #ffffff;
    }

    img {
        width: 377px;
        height: 250px;
    }

    h2 {
        width: 419px;
        font-size: 50px;
        font-weight: 600;
        line-height: 60px;
    }

    h3 {
        font-size: 16px;
        font-weight: 600;
        margin-right: 9px;
    }

    h4 {
        text-transform: uppercase;
        font-size: 16px;
        font-weight: 600;
    }

    .intro {
        background-color: var(--bkg);
        width: 100%;
        height: 549px;
        padding: 23px 0 0 0;
    }

    .container {
        width: 940px;
        height: 100%;
        margin: auto;
    }

    .slider {
        width: 100%;
        height: 49px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .content {
        width: 100%;
        padding-top: 24px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .text {
        height: auto;
    }

    .picture {
        height: auto;
        position: relative;
    }

    .first {
        margin-top: 9px;
        margin-bottom: 26px;
    }

    .second {
        margin-bottom: 26px;
    }
    
    .try {
        width: 30px;
        height: 30px;
        transform: rotate(90deg);
    }
</style>