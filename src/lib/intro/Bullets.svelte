<script>
    export let title;
    export let explain
</script>
<div class="container">
    <img src="arrow.png" alt="Arrow">
    <div class="text">
        <h3>{title}</h3>
        <h5>{explain}</h5>
    </div>
</div>

<style>
    img {
        transform: rotate(90deg);
        width: 30px;
        height: 30px;
        position: absolute;
        bottom: 21px;
    }

    h3 {
        font-size: 16px;
        font-weight: 700;
    }

    h5 {
        font-size: 16px;
        font-weight: 500;
    }

    .container {
        position: relative;
    }

    .text {
        margin-left: 35px;
    }
</style>