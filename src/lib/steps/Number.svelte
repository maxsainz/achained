<script>
    export let tint;
    export let num;
</script>

    <div class="container {tint}" >
        <span>{num}</span>
    </div>

<style>
    span {
        font-size: 22px;
        font-weight: 600;
    }

    .container {
        width: 40px;
        height: 40px;
        border: 2px solid #1e1e1e;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 10;
    }

    .tint-1 {
        background-color: var(--tint-1);
    }

    .tint-2 {
        background-color: var(--tint-2);
    }

    .tint-3 {
        background-color: var(--tint-3);
    }

    .tint-4 {
        background-color: var(--tint-4);
    }
</style>