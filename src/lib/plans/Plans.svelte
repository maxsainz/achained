<script>
    import Card from "./Card.svelte";

</script>

<div class="plans">
    <Card
    title="Free"
    price="$0.00 forever"
    phrase="Best choice to get started"
    reasons={["Accept up to 5 credentials", "Profile creation", "Online support 24/7"]}
    type="tint-1"
    content="About Free"
    />
    <Card
    recomm1={true}
    title="Starter"
    price="$9.99 / month"
    phrase="Best choice for experienced users"
    reasons={["Accept unlimited credentials", "Create up to 20 credentials", "Profile creation", "Sharable link", "Online support 24/7"]}
    type="tint-2"
    content="About Starter"
    />
    <Card
    third={true}
    recomm2={true}
    title="Small"
    price="$49.99 / month"
    phrase="Best choice for small institutions"
    reasons={["Create unlimited credentials", "Institution profile creation", "Online support 24/7", "Priority support", "Automatic credential system"]}
    type="tint-3"
    content="About Small"
    />
    <Card
    last={true}
    title="Custom"
    price="Contact us"
    phrase="Best choice for large enterprises"
    reasons={["Contact experts for more info"]}
    type="tint-4"
    content="About Custom"
    />
</div>

<style>

    .plans {
        background-color: var(--bkg);
        width: 100%;
        height: 825px;
        padding-bottom: 144px;
        display: flex;
        justify-content: center;
        align-items: flex-end;
    }

</style>