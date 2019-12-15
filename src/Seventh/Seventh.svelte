<script>
  import { quintOut, elasticOut, circOut } from "svelte/easing";
  import { fade, scale, fly } from "svelte/transition";
  let html = "images/html.png";
  let css = "images/css.png";
  // duration
  let du = 1500;
  // delay
  let htmld = 1000;
  let cssd = htmld + 2000;
</script>

<style>
  img {
    max-width: 550px;
    height: auto;
    margin: 0 50px;
  }
</style>

<img
  src={html}
  alt=""
  in:fly={{ y: 800, duration: du, delay: htmld, easing: circOut }}
  out:fly={{ x: -300, duration: 1500, easing: circOut }} />

<img
  src={css}
  alt=""
  in:fly={{ y: 800, duration: du, delay: cssd, easing: circOut }}
  out:fly={{ x: -300, duration: 1500, easing: circOut }} />
