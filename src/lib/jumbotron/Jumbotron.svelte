<script>
    import Button from "../Button.svelte";
</script>

<div class="jumbotron">
    <div class="container">
        <h1>Reinventing online credentials.</h1>
        <div class="but-div">
            <Button type=tint-4 content="Credential Hub"/>
            <Button type=primary content="Join the Network"/>
        </div>
    </div>
    <div class="line"></div>
</div>

<style>
    h1 {
        font-size: 75px;
        font-weight: 700;
        z-index: 10;
    }

    .jumbotron {
        position: relative;
    }

    .container {
        width: 100%;
        height: 422px;
        padding: 92px 0 118px 0;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
    }

    .but-div {
        width: 393px;
        display: flex;
        justify-content: space-between;
    }

    .line {
        background-color: var(--primary-alpha);
        width: 100%;
        height: 11px;
        position: absolute;
        top: 148px;
        animation-name: slide-in-from-left;
        animation-duration: 2s;
        animation-iteration-count: 1;
    }

    @keyframes slide-in-from-left {
        0% {
            transform: translateX(-100%);
        }
        100% {
            transform: translateX(0);
        }
    }
</style>