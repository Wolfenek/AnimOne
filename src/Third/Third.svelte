<script>
  import { quintOut } from "svelte/easing";
  import { fade, scale, fly } from "svelte/transition";
  let duHappy = 1500;
  let layHappy = 800;
  let duUp = 1500;
  let layUp = 1000;
  let duSad = 1500;
  let laySad = 2200;
  let duDown = 1500;
  let layDown = 2400;
  let startAnim = false;
  let startAnimTwo = false;
  setTimeout(() => (startAnim = true), 4000);
</script>

<style>
  .startAnim {
    animation: anim1 1.8s linear infinite alternate;
  }

  @keyframes anim1 {
    from {
      transform: translateY(0%);
    }
    to {
      transform: translateY(-20%);
    }
  }

  .startAnimTwo {
    animation: anim2 1.8s linear infinite alternate;
  }

  @keyframes anim2 {
    from {
      transform: translateY(0%);
    }
    to {
      transform: translateY(20%);
    }
  }
</style>

<svg
  width="1456"
  height="354"
  viewBox="0 0 1456 354"
  fill="none"
  xmlns="http://www.w3.org/2000/svg">
  <g id="smileys" out:fly={{ x: 200, duration: 1500, easing: quintOut }}>
    <g
      id="happy"
      in:fly={{ y: 200, duration: duHappy, delay: layHappy, easing: quintOut }}>
      <circle id="Ellipse 8" cx="134.5" cy="177.5" r="134.5" fill="#D3B82A" />
      <path
        id="Subtract"
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M111.277 283.464C191.359 283.464 256.277 218.545 256.277
        138.464C256.277 131.171 255.739 124.004 254.7 117C264.021 135.3 269.277
        156.018 269.277 177.964C269.277 252.246 209.06 312.464 134.777
        312.464C88.8291 312.464 48.2622 289.423 24 254.266C48.2815 272.595
        78.5101 283.464 111.277 283.464Z"
        fill="#AB9109" />
      <ellipse id="Ellipse 11" cx="77" cy="138" rx="16" ry="31" fill="black" />
      <ellipse id="Ellipse 12" cx="193" cy="138" rx="16" ry="31" fill="black" />
      <path
        id="Rectangle 25"
        d="M53 224.425C53 213.237 67.1724 207.511 76.0137 214.368C118.336
        247.187 158.27 242.671 193.824 214.936C202.66 208.043 217 213.739 217
        224.946V224.946C217 228.933 215.031 232.698 211.735 234.942C145.378
        280.133 120.813 272.499 58.882 234.898C55.227 232.679 53 228.701 53
        224.425V224.425Z"
        fill="black" />
    </g>
    <g
      id="sad"
      in:fly={{ y: 200, duration: duSad, delay: laySad, easing: quintOut }}>
      <circle id="Ellipse 13" cx="991.5" cy="161.5" r="134.5" fill="#D3B82A" />
      <path
        id="Subtract_2"
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M968.277 267.464C1048.36 267.464 1113.28 202.545 1113.28
        122.464C1113.28 115.171 1112.74 108.004 1111.7 101C1121.02 119.3 1126.28
        140.018 1126.28 161.964C1126.28 236.246 1066.06 296.464 991.777
        296.464C945.829 296.464 905.262 273.423 881 238.266C905.281 256.595
        935.51 267.464 968.277 267.464Z"
        fill="#AB9109" />
      <ellipse id="Ellipse 14" cx="934" cy="122" rx="16" ry="31" fill="black" />
      <ellipse
        id="Ellipse 15"
        cx="1050"
        cy="122"
        rx="16"
        ry="31"
        fill="black" />
      <path
        id="Rectangle 26"
        d="M1074 218.608C1074 229.796 1059.83 235.522 1050.99 228.666C1008.66
        195.847 968.73 200.363 933.176 228.098C924.34 234.991 910 229.294 910
        218.088V218.088C910 214.101 911.969 210.336 915.265 208.092C981.622
        162.9 1006.19 170.534 1068.12 208.136C1071.77 210.355 1074 214.332 1074
        218.608V218.608Z"
        fill="black" />
    </g>
    <path
      id="up"
      in:fly={{ y: 200, duration: duUp, delay: layUp, easing: quintOut }}
      class:startAnim
      d="M467.374 5.62564C460.54 -1.20856 449.46 -1.20856 442.626
      5.62564L331.256 116.995C324.422 123.829 324.422 134.91 331.256
      141.744C338.09 148.578 349.171 148.578 356.005 141.744L455 42.7487L553.995
      141.744C560.829 148.578 571.91 148.578 578.744 141.744C585.578 134.91
      585.578 123.829 578.744 116.995L467.374 5.62564ZM472.5 336L472.5 18L437.5
      18L437.5 336L472.5 336Z"
      fill="#1FBA12" />
    <path
      id="down"
      in:fly={{ y: 200, duration: duDown, delay: layDown, easing: quintOut }}
      class={startAnim ? 'startAnimTwo' : ''}
      d="M1314.63 348.374C1321.46 355.209 1332.54 355.209 1339.37
      348.374L1450.74 237.005C1457.58 230.171 1457.58 219.09 1450.74
      212.256C1443.91 205.422 1432.83 205.422 1425.99 212.256L1327
      311.251L1228.01 212.256C1221.17 205.422 1210.09 205.422 1203.26
      212.256C1196.42 219.09 1196.42 230.171 1203.26 237.005L1314.63
      348.374ZM1309.5 18L1309.5 336L1344.5 336L1344.5 18L1309.5 18Z"
      fill="#E80101" />
  </g>
</svg>
