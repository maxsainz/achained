<script>
    import Button from "../Button.svelte";
    import Tick from "./Tick.svelte";

    export let third = false;
    export let last = false;
    export let recomm1 = false;
    export let recomm2 = false;
    export let title;
    export let price;
    export let phrase;
    export let reasons;
    export let type;
    export let content;
</script>

<div>
    <div class="noshow" class:recomm1>
        <h5>Recommended for users</h5>
    </div>
    <div class="noshow" class:recomm2>
        <h5>Recommended for institutions</h5>
    </div>
    <div class="card" class:last class:third>
        <h2>{title}</h2>
        <h3>{price}</h3>
        <h5>{phrase}</h5>
        <div class="line {type}"></div>
        <div class="ticks">
            {#each reasons as reason}
                <Tick reason={reason}/>
            {/each}
        </div>
        <div class="button">
            <Button type={type} content={content}/>
        </div>
    </div>
</div>


<style>
    h2 {
        font-size: 50px;
        font-weight: 600;
        line-height: 60px;
        padding-left: 21px;
    }

    h3 {
        position: relative;
        bottom: 6px;
        font-size: 20px;
        font-weight: 700;
        padding-left: 21px;
    }

    h5 {
        font-size: 16px;
        font-weight: 500;
        padding-left: 21px;
    }

    .noshow {
        display: none;
    }

    .recomm1 {
        display: block;
        background-color: var(--tint-2);
        width: 322px;
        height: 44px;
        border-top: 2px solid #1e1e1e;
        border-left: 2px solid #1e1e1e;
        display: flex;
        align-items: center;
    }

    .recomm2 {
        display: block;
        background-color: var(--tint-3);
        width: 322px;
        height: 44px;
        border-top: 2px solid #1e1e1e;
        border-left: 2px solid #1e1e1e;
        border-right: 2px solid #1e1e1e;
        display: flex;
        align-items: center;
    }

    .card {
        background-color: #ffffff;
        position: relative;
        width: 322px;
        height: 537px;
        padding-top: 8px;
        border-top: 2px solid #1e1e1e;
        border-left: 2px solid #1e1e1e;
        border-bottom: 2px solid #1e1e1e;
    }

    .third {
        border-right: 2px solid #1e1e1e;
    }

    .last {
        border-right: 2px solid #1e1e1e;
        border-left: none;
    }

    .line {
        width: 100%;
        height: 4px;
        margin-top: 16px;
        margin-bottom: 16px;
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

    .ticks {
        padding-left: 21px;
    }

    .button {
        width: 100%;
        position: absolute;
        bottom: 60px;
        display: flex;
        justify-content: center;
    }
</style>