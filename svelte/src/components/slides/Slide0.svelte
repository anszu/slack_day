<script>
    import Transition from '/src/components/Transition.svelte';
</script>

<Transition>
    <h2>Hello!</h2>
    <ul>
        <li>JavaScript framework</li>
        <li>released in 2016</li>
    </ul>
    <quote>
        Whereas traditional frameworks like React and Vue do the bulk of their work in the browser,
        Svelte shifts that work into a compile step that happens when you build your app.
    </quote>
    <br><br>
    <quote>
        Instead of using techniques like virtual DOM diffing,
        Svelte writes code that surgically updates the DOM when the state of your app changes.
    </quote>
</Transition>

<style>
    quote {
        margin: 2rem;
        text-align: center;
        width: 18rem;
        font-style: italic;
    }
</style>


