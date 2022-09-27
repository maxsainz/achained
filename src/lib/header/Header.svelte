<script>
    import Hamburger from "./Hamburger.svelte";
import Logo from "./Logo.svelte";
    import Searchbar from "./Searchbar.svelte";


</script>

<div class="header">
    <div class="logo">
        <Logo />
    </div>
    <div class="search-bar">
        <Searchbar />
    </div>
    <div class="hamburger">
        <Hamburger />
    </div>
</div>

<style>
    .header {
        background-color: #ffffff;
        width: 100%;
        height: 80px;
        padding: 0 72px 0 72px;
        border-bottom: 2px solid #ededed;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        align-items: center;
    }

    .logo {
        justify-self: self-start;
    }

    .search-bar {
        justify-self: center;
    }

    .hamburger {
        justify-self: self-end;
    }
</style>