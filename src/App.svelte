<script>
  import Cells from "./lib/cells/Cells.svelte";
  import Footer from "./lib/footer/Footer.svelte";
  import Header from "./lib/header/Header.svelte";
  import Intro from "./lib/intro/Intro.svelte";
  import Jumbotron from "./lib/jumbotron/Jumbotron.svelte";
  import Plans from "./lib/plans/Plans.svelte";
  import Steps from "./lib/steps/Steps.svelte";
  import Title from "./lib/Title.svelte";

</script>


  <header>
    <Header />
  </header>
  <main>
    <section class="first">
      <Jumbotron />
    </section>
    <section>
      <Intro />
    </section>
    <section>
      <Title title="What is Achained?"/>
      <Cells />
    </section>
    <section>
      <Title title="Explore our pricing"/>
      <Plans />
    </section>
    <section>
      <Title title="How does Achained work?"/>
    </section>
    <Steps />
  </main>
  <footer>
    <div class="line"></div>
    <Footer />
  </footer>


<style>

  header {
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
  }

  main {
    margin-top: 80px;
  }
  
  .line {
    width: 100%;
    height: 11px;
    background-color: var(--primary-alpha);
  }

</style>
