<script>
  import { quintOut, backOut } from "svelte/easing";
  import { fade, fly, slide } from "svelte/transition";
  let brain = "images/brain.png";
  // duration
  let du = 2000;
  // delay
  let lay1 = 2500;
  let lay2 = 5000;
  let startAnim = false;
</script>

<style>
  img {
    margin-bottom: 200px;
  }

  .startAnim {
    animation: wheel 3s infinite linear;
    transform-origin: center;
    transform-box: fill-box;
  }

  @keyframes wheel {
    0%,
    100% {
      transform: rotate(0deg);
    }
    25% {
      transform: rotate(15deg);
    }
    75% {
      transform: rotate(-15deg);
    }
  }

  .scaleUp {
    animation: scale 3s infinite linear;
    transform-origin: center;
    transform-box: fill-box;
  }
  @keyframes scale {
    0%,
    100% {
      transform: scale(1);
    }
    25% {
      transform: scale(1.1);
    }
    75% {
      transform: scale(0.9);
    }
  }

  .goDown {
    animation: go 3s infinite linear;
    transform-origin: center;
    transform-box: fill-box;
  }
  @keyframes go {
    0%,
    100% {
      transform: translateY(0px);
    }
    25% {
      transform: translateY(40px);
    }
    75% {
      transform: translateY(-40px);
    }
  }
</style>

<div out:fly={{ y: -200, duration: 1500, easing: quintOut }}>
  <svg
    width="270"
    height="270"
    viewBox="0 0 270 270"
    fill="none"
    xmlns="http://www.w3.org/2000/svg">
    <g
      id="purple"
      class={startAnim === true ? 'goDown' : ''}
      in:fly={{ x: -100, duration: du, delay: 500, easing: backOut }}>
      <circle
        id="Ellipse 22"
        cx="134.5"
        cy="134.5"
        r="134.5"
        fill="#C556F9"
        fill-opacity="0.8" />
      <path
        id="Subtract"
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M111.277 240.464C191.359 240.464 256.277 175.545 256.277
        95.4639C256.277 88.171 255.739 81.0038 254.7 74C264.021 92.3003 269.277
        113.018 269.277 134.964C269.277 209.246 209.06 269.464 134.777
        269.464C88.8291 269.464 48.2622 246.423 24 211.266C48.2815 229.595
        78.5101 240.464 111.277 240.464Z"
        fill="#C556F9" />
      <ellipse id="Ellipse 23" cx="77" cy="95" rx="16" ry="31" fill="black" />
      <ellipse id="Ellipse 24" cx="193" cy="95" rx="16" ry="31" fill="black" />
      <path
        id="Rectangle 74"
        d="M217 191.608C217 202.796 202.828 208.522 193.986 201.666C151.664
        168.847 111.73 173.363 76.1764 201.098C67.3403 207.991 53 202.294 53
        191.088V191.088C53 187.101 54.9694 183.336 58.2646 181.092C124.622 135.9
        149.187 143.534 211.118 181.136C214.773 183.355 217 187.332 217
        191.608V191.608Z"
        fill="black" />
    </g>
  </svg>

  <img
    src={brain}
    alt=""
    class:startAnim
    in:fly={{ y: -100, duration: du, delay: lay1, easing: backOut }} />

  <svg
    width="391"
    height="403"
    viewBox="0 0 391 403"
    fill="none"
    xmlns="http://www.w3.org/2000/svg">
    <g
      id="look"
      on:introend={() => (startAnim = true)}
      class={startAnim === true ? 'scaleUp' : ''}
      in:fly={{ x: 100, duration: du, delay: lay2, easing: backOut }}>
      <g id="Vector">
        <path
          d="M179.874 209.608C183.401 206.096 189.121 206.095 192.65
          209.605L194.247 211.194C197.776 214.704 197.778 220.396 194.251
          223.908L17.0215 400.365C13.4943 403.877 7.77407 403.878 4.2451
          400.368L2.64765 398.779C-0.881323 395.269 -0.88273 389.577 2.64451
          386.065L179.874 209.608Z"
          fill="#6D6D6D" />
        <path
          d="M181.735 173.906C185.112 170.251 190.827 170.011 194.5
          173.372L231.08 206.837C234.753 210.198 234.993 215.885 231.617
          219.541L219.388 232.778C216.011 236.433 210.296 236.672 206.623
          233.312L170.043 199.846C166.37 196.486 166.13 190.798 169.507
          187.143L181.735 173.906Z"
          fill="#6D6D6D" />
      </g>
      <circle id="Ellipse 6" cx="277" cy="114" r="114" fill="#0F006F" />
      <circle id="Ellipse 7" cx="277" cy="114" r="94" fill="#CEFFFC" />
    </g>
  </svg>

</div>
