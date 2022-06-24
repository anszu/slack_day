<script>
    import { fly } from 'svelte/transition';
</script>

<div in:fly="{{ y: 100, duration: 500 }}">
    <slot></slot>
</div>


