<script>
    export let currentSlide;
    export let slidesLength;
    export let showPrevious;
    export let showNext;
</script>

<footer>
    {#if currentSlide > 0}
        <button on:click={ showPrevious }>
            ⇦
        </button>
    {/if}

    {#if currentSlide < slidesLength - 1}
        <button on:click={ showNext }>
            ⇨
        </button>
    {/if}
</footer>

<style>
    button {
        font-size: 1rem;
        color: #ff3e00;
        width: 6rem;
        margin-left: 1rem;
    }

    footer {
        width: 100%;
        justify-content: center;
        display: flex;
    }
</style>