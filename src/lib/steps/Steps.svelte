<script>
    import Explain from "./Explain.svelte";
    import Number from "./Number.svelte";

    let inviewone = false;
    let inviewtwo = false;
    let inviewthree = false;
    let inviewfour = false;

    function actionWhenInViewportOne(e) {
        const observer = new IntersectionObserver(entries => {
        if(entries[0].isIntersecting) {
            inviewone = true;
        }
        });
        observer.observe(e);
    }

    function actionWhenInViewportTwo(e) {
        const observer = new IntersectionObserver(entries => {
        if(entries[0].isIntersecting) {
            inviewtwo = true;
        }
        });
        observer.observe(e);
    }  

    function actionWhenInViewportThree(e) {
        const observer = new IntersectionObserver(entries => {
        if(entries[0].isIntersecting) {
            inviewthree = true;
        }
        });
        observer.observe(e);
    } 

    function actionWhenInViewportFour(e) {
        const observer = new IntersectionObserver(entries => {
        if(entries[0].isIntersecting) {
            inviewfour = true;
        }
        });
        observer.observe(e);
    }  

</script>

<div class="steps">
    <div class="container">
        <div class="line"></div>
        <div class="step-1">
            <div class="step">
                <img src="step1.png" alt="Step 1" class:inview={inviewone} use:actionWhenInViewportOne>
                <Number tint="tint-1" num="1"/>
                <div class="cont-1">
                    <Explain title="Unique ID:" text="A credential with a unique ID is created"/>
                </div>
            </div> 
        </div>
        <div class="step-2">
            <div class="step">
                <div class="cont-2">
                    <Explain title="Parties IDs:" text="Both parties ID's are included inside the credential"/>
                </div>
                <Number tint="tint-2" num="2"/>
                <img src="step2.png" alt="Step 2" class:inview={inviewtwo} use:actionWhenInViewportTwo>
            </div> 
        </div>
        <div class="step-3">
            <div class="step">
                <img src="step3.png" alt="Step 3" class:inview={inviewthree} use:actionWhenInViewportThree>
                <Number tint="tint-3" num="3"/>
                <div class="cont-3">
                    <Explain title="Reach agreement:" text="Both parties accept and agree to upload the credential"/>
                </div>
            </div> 
        </div>
        <div class="step-4">
            <div class="step">
                <div class="cont-4">
                    <Explain title="Create block:" text="The credential is uploaded to the blockchain"/>
                </div>
                <Number tint="tint-4" num="4"/>
                <img src="step4.png" alt="Step 4" class:inview={inviewfour} use:actionWhenInViewportFour>
            </div> 
        </div> 
    </div>
</div>

<style>
    .line {
    position: absolute;
    top: 107px;
    left: 343px;
    height: 841px;
    width: 100px;
    border-right: 2px dashed #1e1e1e;
}

    .steps {
        width: 100%;
        height: 1147px;
    }

    .container {
        width: 960.1px;
        height: 1046;
        margin: auto;
        position: relative;
    }

    .step {
        width: auto;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .step-1 {
        display: inline-block;
        margin-left: 147px;
        margin-bottom: 62px;
    }

    .step-1 img {
        width: 150px;
        height: 211.02px;
        margin-right: 125px;
        transform: translateX(-100%);
        opacity: 0;
        transition: all 1s linear 0.75s;
    }

    .cont-1 {
        margin-left: 52px;
    }

    .step-2 {
        display: inline-block;
        margin-bottom: 60px;
    }

    .step-2 img {
        width: 189px;
        height: 227px;
        margin-left: 125px;
        transform: translateX(100%);
        opacity: 0;
        transition: all 1s linear 0.75s;
    }

    .cont-2 {
        margin-right: 49px;
    }
    
    .step-3 {
        display: inline-block;
        margin-left: 95px;
        margin-bottom: 77px;
    }

    .step-3 img {
        width: 202px;
        height: 216px;
        margin-right: 125px;
        transform: translateX(-100%);
        opacity: 0;
        transition: all 1s linear 0.75s;
    }

    .cont-3 {
        margin-left: 52px;
    }

    .step-4 {
        display: inline-block;
    }

    .step-4 img {
        width: 373;
        height: 193px;
        margin-left: 125px;
        transform: translateX(100%);
        opacity: 0;
        transition: all 1s linear 0.75s;
    }

    .cont-4 {
        margin-right: 49px;
    }

    .step .inview {
        transform: translateX(0);
        opacity: 1;
    }
</style>