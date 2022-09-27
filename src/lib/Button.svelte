<script>
    export let type;
    export let content;
</script>

<a href="index.html" class={type}>
    <h3>{content}</h3>
</a>

<style>
    a {
        display: flex;
        width: 183px;
        height: 49px;
        border: 2px solid #1e1e1e;
        border-radius: 23.5px;
        text-decoration: none;
        justify-content: center;
        align-items: center;
        transition: all 0.2s ease-out 0s;
    }

    a:hover {
        box-shadow: 0 3.5px #1e1e1e;
        transform: translateY(-0.25em);
    }

    h3 {
        font-size: 16px;
        font-weight: 600;
        color: #1e1e1e;
    }

    .primary {
        background-color: var(--primary-color);
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