<script>
    export let promo
</script>

<style>
    .wrapper {
        background-color: white;
        border-radius: 4px;
        margin-bottom: 12px;
        padding: 12px;
    }

    h2 {
        font-size: 21px;
        margin: 0 0 4px;
    }

    p {
        margin: 0;
    }

    .outlet-name {
        font-size: 12px;
        font-weight: 600;
        margin: 0 0 4px;
        opacity: .54;
    }
</style>

<div class="wrapper">
    <p class="outlet-name">
        {promo.outlet}
    </p>
    <h2>{promo.title}</h2>
    <p>
        {promo.description}
    </p>
</div>
