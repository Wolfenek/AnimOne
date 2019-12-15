<script>
  import First from "./First/First.svelte";
  import Second from "./Second/Second.svelte";
  import Third from "./Third/Third.svelte";
  import Fourth from "./Fourth/Fourth.svelte";
  import Fifth from "./Fifth/Fifth.svelte";
  import Sixth from "./Sixth/Sixth.svelte";
  import Seventh from "./Seventh/Seventh.svelte";
  import Eighth from "./Eighth/Eighth.svelte";
  import Ninth from "./Ninth/Ninth.svelte";
  import Ten from "./Ten/Ten.svelte";
  import Eleven from "./Eleven/Eleven.svelte";
  import Twelve from "./Twelve/Twelve.svelte";
  import Thirteen from "./Thirteen/Thirteen.svelte";
  import Fourteen from "./Fourteen/Fourteen.svelte";
  import Fifteen from "./Fifteen/Fifteen.svelte";
  let bg = "images/bg1.png";
  let scene = 0;

  const wait = time => new Promise(tick => setTimeout(tick, time));
  async function nextScene(time, number) {
    scene = number;
    await wait(time);
    scene = 0;
    await wait(1500);
  }
  async function handleMouseDown() {
    // await nextScene(8000, 1);
    // await nextScene(15000, 2);
    // await nextScene(8000, 3);
    // await nextScene(8000, 4);
    // await nextScene(8000, 5);
    // await nextScene(8000, 6);
    // await nextScene(8000, 7);
    // await nextScene(8000, 8);
    // await nextScene(8000, 9);
    // await nextScene(8000, 10);
    // await nextScene(8000, 11);
    // await nextScene(12000, 12);
    // await nextScene(12000, 13);
    // await nextScene(12000, 14);
    await nextScene(16000, 15);
  }
</script>

<style>
  .wrapper {
    min-height: 100vh;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    background-color: #fff;
    background-image: linear-gradient(
        90deg,
        transparent 79px,
        #abced4 79px,
        #abced4 81px,
        transparent 81px
      ),
      linear-gradient(#eee 0.1em, transparent 0.1em);
    background-size: 100% 1.2em;
    overflow-x: hidden;
    overflow-y: hidden;
  }
</style>

<svelte:window on:mousedown={handleMouseDown} />

<div class="wrapper">
  {#if scene === 1}
    <First />
  {:else if scene === 2}
    <Second />
  {:else if scene === 3}
    <Third />
  {:else if scene === 4}
    <Fourth />
  {:else if scene === 5}
    <Fifth />
  {:else if scene === 6}
    <Sixth />
  {:else if scene === 7}
    <Seventh />
  {:else if scene === 8}
    <Eighth />
  {:else if scene === 9}
    <Ninth />
  {:else if scene === 10}
    <Ten />
  {:else if scene === 11}
    <Eleven />
  {:else if scene === 12}
    <Twelve />
  {:else if scene === 13}
    <Thirteen />
  {:else if scene === 14}
    <Fourteen />
  {:else if scene === 15}
    <Fifteen />
  {:else}
    <div />
  {/if}
</div>
