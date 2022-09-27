<script>
    export let title;
    export let points;
</script>

<div class="list">
    
    <h3>{title}</h3>
    <ul>
        {#each points as point}
            <li><a href="index.html">{point}</a></li>
        {/each}
    </ul>
</div>

<style>
    h3 {
        font-size: 16px;
        font-weight: 600;
        margin-bottom: 17px;
    }

    li {
        list-style-type: none;
        margin-bottom: 11px;
    }

    a {
        text-decoration: none;
        color: #1e1e1e;
        font-size: 15px;
        font-weight: 400;
    }
</style>