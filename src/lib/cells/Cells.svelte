<script>
  import Button from "../Button.svelte";


</script>

<div class="container">
    <div class="cells">
        <div class="cell one">
            <h3>Blockchain powered</h3>
            <h5>Make your credentials instantly verifiable</h5>
            <div class="inner">
                <Button type="tint-1" content="Learn more"/>
            </div>
        </div>
        <div class="cell three">
            <h3>Connect with platforms</h3>
            <h5>Share your credentials across multiple platforms</h5>
            <div class="inner">
                <Button type="tint-3" content="Learn more"/>
            </div>
        </div>
        <div class="cell two">
            <h3>Verify in a single click</h3>
            <h5>Check the validity of credentials in seconds</h5>
            <div class="inner">
                <Button type="tint-2" content="Learn more"/>
            </div>
        </div>
        <div class="cell four">
            <h3>Want to know more?</h3>
            <h5>Understand better the tech behind Achained</h5>
            <div class="inner">
                <Button type="tint-4" content="Learn more"/>
            </div>
        </div>
    </div>
    <div class="img"></div>
</div>

<style>
    h3 {
        font-size: 20px;
        font-weight: 700;
        margin-bottom: 10px;
    }

    h5 {
        font-size: 20px;
        font-weight: 500;
        width: 262px;
        margin-bottom: 40px;
    }

    .inner {
        width: 100%;
        display: flex;
        justify-content: center;
    }

    .container {
        width: 100%;
        height: 542px;
        display: flex;
    }

    .cells {
        height: 100%;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr;
    }

    .cell {
        width: 320px;
        padding: 39px 20px 0 20px;
    }

    .one {
        background-color: var(--tint-1);
    }

    .two {
        background-color: var(--tint-2);
    }

    .three {
        background-color: var(--tint-3);
    }

    .four {
        background-color: var(--tint-4);
    }

    .img {
        width: 100%;
        height: 100%;
        background-image: url("chairs.jpg");
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }

</style>

