<script lang="ts">
    import logo from '/src/assets/svelte.png'
</script>

<header>
    <img src={logo} alt="Svelte Logo" />
    <h1>Svelte</h1>
</header>

<style>
    img {
        height: 4rem;
        width: 4rem;
    }

    h1 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 2rem;
        font-weight: 100;
        line-height: 1.1;
        max-width: 14rem;
    }

    header {
        justify-content: center;
        display: flex;
        width: 100%;
    }
</style>