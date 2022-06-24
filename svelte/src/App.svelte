<script lang="ts">
  import Header from '/src/components/Header.svelte'
  import Footer from '/src/components/Footer.svelte'
  import Slide0 from '/src/components/slides/Slide0.svelte'
  import Slide1 from '/src/components/slides/Slide1.svelte'
  import Slide2 from '/src/components/slides/Slide2.svelte'
  import Slide3 from '/src/components/slides/Slide3.svelte'
  import Slide4 from '/src/components/slides/Slide4.svelte'
  import Slide5 from '/src/components/slides/Slide5.svelte'
  import Slide6 from '/src/components/slides/Slide6.svelte'
  import Slide7 from '/src/components/slides/Slide7.svelte'
  import Slide8 from '/src/components/slides/Slide8.svelte'

  let currentSlide = 0;
  const slides = [Slide0, Slide1, Slide2, Slide3, Slide4, Slide5, Slide6, Slide7, Slide8];

  const showNext = () => {
    currentSlide += 1;
  }

  const showPrevious = () => {
    currentSlide -= 1;
  }

  $: console.log(currentSlide);
</script>

<Header />

<main>
  <svelte:component this={ slides[currentSlide] }/>
</main>

<Footer
  currentSlide={ currentSlide }
  slidesLength={ slides.length }
  showPrevious={ showPrevious }
  showNext={ showNext }
/>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    padding: 1em;
    margin: 0 auto;
    width: 32rem;
    min-height: 28rem;
    font-size: 1.5rem;
  }
</style>
