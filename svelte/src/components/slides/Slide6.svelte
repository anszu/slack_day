<script>
    import Transition from '/src/components/Transition.svelte';
    import dynamic from '/src/assets/dynamic.png'
</script>

<Transition>
    <h2>Dynamic components</h2>
    <img src={dynamic} alt="Svelte Code" />
</Transition>