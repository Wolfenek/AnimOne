<script>
  import { quintOut } from "svelte/easing";
  import { fade, fly } from "svelte/transition";
  let ffc2 = "images/ffc2.png";

</script>

<style>
</style>

<img src={ffc2} alt="" in:fade={{ duration: 500 }} out:fly={{ x:-200, duration: 1500, easing: quintOut }} />