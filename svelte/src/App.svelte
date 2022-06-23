<script lang="ts">
  import logo from './assets/svelte.png'
  import Slide0 from './slides/Slide0.svelte'
  import Slide1 from './slides/Slide1.svelte'
  import Slide2 from './slides/Slide2.svelte'
  import Slide3 from './slides/Slide3.svelte'
  import Slide4 from './slides/Slide4.svelte'
  import Slide5 from './slides/Slide5.svelte'
  import Slide6 from './slides/Slide6.svelte'
  import Slide7 from './slides/Slide7.svelte'
  import Slide8 from './slides/Slide8.svelte'
  import Slide9 from './slides/Slide9.svelte'
  import Slide10 from './slides/Slide10.svelte'

  let currentSlide = 0;

  let components = [Slide0, Slide1, Slide2, Slide3, Slide4, Slide5, Slide6, Slide7, Slide8, Slide9, Slide10];

  const showNext = () => {
    currentSlide = currentSlide < 10 ? currentSlide + 1 : 0;
  }

  $: console.log(currentSlide);
</script>

<main>
  <img src={logo} alt="Svelte Logo" />
  <h1>Svelte</h1>

  <svelte:component this={ components[currentSlide] }/>

  <button on:click={ showNext }>
    ->
  </button>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

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
    margin: 1rem auto;
    max-width: 14rem;
  }
</style>
