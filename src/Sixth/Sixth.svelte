<script>
  import { quintOut, elasticOut, circOut, bounceOut } from "svelte/easing";
  import { fade, scale, fly } from "svelte/transition";
  let hs = "images/hs.png";
  let ball = "images/ball.png";
  // duration
  let du = 2000;
  // delay
  let hsd = 500;
  let balld = hsd + 500;
</script>

<style>
  img {
    max-width: 550px;
    height: auto;
    margin: 0 50px;
  }
  
</style>

<img
  src={hs}
  alt=""
  in:fly={{ y: -800, duration: du, delay: hsd, easing: circOut }}
  out:fly={{ y: 500, duration: 1500, easing: circOut }} />

<img
  src={ball}
  alt=""
  in:fly={{ opacity: 1, y: -1000, duration: 3200, delay: balld, easing: bounceOut }}
  out:fly={{ y: 500, duration: 1500, easing: circOut }} />
