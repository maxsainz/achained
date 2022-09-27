<script>
    export let reason;
</script>

<div class="tick">
    <img src="done.png" alt="Done">
    <h5>{reason}</h5>
</div>

<style>

    img {
        width: 30px;
        height: 30px;
        margin-right: 5px;
    }

    h5 {
        font-size: 16px;
        font-weight: 500;
    }

    .tick {
        width: auto;
        height: 30px;
        margin-bottom: 16px;
        display: flex;
        justify-content: flex-start;
        align-items: center;
    }

</style>