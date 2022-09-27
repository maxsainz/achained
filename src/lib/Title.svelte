<script>

    export let title;
    let inview = false;

    function actionWhenInViewport(e) {
        const observer = new IntersectionObserver(entries => {
        if(entries[0].isIntersecting) {
            inview = true;
        }
        });
        observer.observe(e);
    }  

</script>

    <div class="title">
        <div class="container">
            <h2 use:actionWhenInViewport>{title}</h2>
        </div>
        <div class="line" class:inview></div>
    </div>

<style>

    h2 {
        font-size: 50px;
        font-weight: 700;
        z-index: 10;
    }

    .title {
        padding-top: 66px;
        padding-bottom: 64px;
        position: relative;
    }

    .container {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .line {
        background-color: var(--primary-alpha);
        width: 100%;
        height: 11px;
        position: absolute;
        top: 100px;
        transform: translateX(-100%);
        transition: transform 1s linear 0.5s;
    }

    .inview {
        transform: translateX(0);
    }

</style>