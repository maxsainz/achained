<script>

    export let current = 'right';

    function moveSlider() {
        const id = this.id;
        if(id === "second") {
            current = 'left';
        } else {
            current = 'right';
        }
    }

</script>

<div class="container">
    <div class="slider">
        <div id="slide" class="slide" class:left="{current === 'left'}"></div>
        <button id="first" class="button" on:click={moveSlider}>
            <h3>For users</h3>
        </button>
        <button class="button" id="second" on:click={moveSlider}>
            <h3 class="change">For institutions</h3>
        </button>
    </div>
</div>

<style>
    button {
        border: none;
        color: #1e1e1e;
        text-decoration: none;
        display: inline-block;
        width: 185px;
        height: 100%;
        background-color: #ffffff;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 23.5px;
    }

    button :hover {
        cursor: pointer;
    }

    h3 {
        z-index: 10;
        font-size: 16px;
        font-weight: 600;
    }

    .container {
        background-color:#ffffff;
        width: 393px;
        height: 100%;
        border-radius: 23.5px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .slider {
        position: relative;
        width: 376px;
        height: 37px;
        border-radius: 23.5px;
        border: 2px solid #1e1e1e;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .slide {
        z-index: 1;
        position: absolute;
        top: 0;
        left: 0;
        width: 185px;
        height: 100%;
        border-radius: 23.5px;
        background-color: var(--primary-color);
        outline: 2px solid #1e1e1e;
        transition: left 0.1s linear 0s;
    }
    

    .left {
        left: 50.5%;
    }

    .change {
        margin-left: 5px;
    }
</style>