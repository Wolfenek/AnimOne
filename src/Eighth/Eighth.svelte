<script>
  import { quintOut, linear } from "svelte/easing";
  import { fade, fly, draw } from "svelte/transition";
  // duration
  let du = 1000;
  // delay
  let dami = 500;
  let bub1 = dami + du;
  let bub2 = bub1;
  let bubble = bub2 + du;
  let kid = bubble + 3000;
  let gear = kid + du;
  let startAnim = false;
</script>

<style>
  .startAnim {
    animation: wheel 7s infinite linear;
    transform-origin: center;
    transform-box: fill-box;
  }

  @keyframes wheel {
    from {
      transform: rotateZ(0deg);
    }
    to {
      transform: rotateZ(-360deg);
    }
  }
</style>

<svg
  width="1058"
  height="940"
  viewBox="0 0 1058 940"
  fill="none"
  xmlns="http://www.w3.org/2000/svg">
  <g id="mind" out:fly={{ y: 200, duration: 1500, easing: linear }}>
    <g id="bub2">
      <circle
        in:draw={{ duration: 2500, delay: bub2, easing: linear }}
        id="Ellipse 2"
        cx="455.5"
        cy="509.5"
        r="71.5"
        stroke="black"
        stroke-width="12" />
    </g>
    <g
      id="Dude"
      in:fly={{ y: 200, duration: du, delay: dami, easing: quintOut }}>
      <g id="Ellipse" filter="url(#filter0_d)">
        <path
          d="M292.587 792.734C292.587 869.648 232.226 932 157.767 932C83.3073
          932 22.9462 869.648 22.9462 792.734C22.9462 715.819 83.3073 653.467
          157.767 653.467C232.226 653.467 292.587 715.819 292.587 792.734Z"
          fill="#FFF3E6" />
      </g>
      <path
        id="Vector 7.5"
        d="M273.814 851.687C233.456 897.824 130.564 962.416 41.8675
        851.687L40.012 857.454L76.1957 903.591L130.471 928.582H185.675C199.591
        922.655 228.353 909.839 232.064 905.994C235.775 902.149 255.877 884.207
        265.464 875.717L273.814 851.687Z"
        fill="#D7A97F" />
      <g id="Ellipse (Stroke)">
        <mask id="path-7-inside-1" fill="white">
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M157.767 924.67C227.944 924.67 285.25 865.833 285.25
            792.734C285.25 719.634 227.944 660.797 157.767 660.797C87.5889
            660.797 30.2833 719.634 30.2833 792.734C30.2833 865.833 87.5889
            924.67 157.767 924.67ZM157.767 932C232.226 932 292.587 869.648
            292.587 792.734C292.587 715.819 232.226 653.467 157.767
            653.467C83.3073 653.467 22.9462 715.819 22.9462 792.734C22.9462
            869.648 83.3073 932 157.767 932Z" />
        </mask>
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M157.767 924.67C227.944 924.67 285.25 865.833 285.25 792.734C285.25
          719.634 227.944 660.797 157.767 660.797C87.5889 660.797 30.2833
          719.634 30.2833 792.734C30.2833 865.833 87.5889 924.67 157.767
          924.67ZM157.767 932C232.226 932 292.587 869.648 292.587
          792.734C292.587 715.819 232.226 653.467 157.767 653.467C83.3073
          653.467 22.9462 715.819 22.9462 792.734C22.9462 869.648 83.3073 932
          157.767 932Z"
          fill="black" />
        <path
          d="M277.25 792.734C277.25 861.657 223.287 916.67 157.767
          916.67V932.67C232.601 932.67 293.25 870.009 293.25
          792.734H277.25ZM157.767 668.797C223.287 668.797 277.25 723.81 277.25
          792.734H293.25C293.25 715.458 232.601 652.797 157.767
          652.797V668.797ZM38.2833 792.734C38.2833 723.81 92.2456 668.797
          157.767 668.797V652.797C82.9322 652.797 22.2833 715.458 22.2833
          792.734H38.2833ZM157.767 916.67C92.2456 916.67 38.2833 861.657 38.2833
          792.734H22.2833C22.2833 870.009 82.9322 932.67 157.767
          932.67V916.67ZM284.587 792.734C284.587 865.477 227.565 924 157.767
          924V940C236.887 940 300.587 873.82 300.587 792.734H284.587ZM157.767
          661.467C227.565 661.467 284.587 719.99 284.587 792.734H300.587C300.587
          711.647 236.887 645.467 157.767 645.467V661.467ZM30.9462
          792.734C30.9462 719.99 87.9683 661.467 157.767 661.467V645.467C78.6463
          645.467 14.9462 711.647 14.9462 792.734H30.9462ZM157.767 924C87.9683
          924 30.9462 865.477 30.9462 792.734H14.9462C14.9462 873.82 78.6463 940
          157.767 940V924Z"
          fill="black"
          mask="url(#path-7-inside-1)" />
      </g>
      <g id="Vector" filter="url(#filter1_d)">
        <path
          d="M11 691.346C12.7224 694.455 16.4491 717.742 17.5765 786.019C38.2456
          791.616 51.2421 742.957 55.1567 717.929C62.5161 726.79 78.7382 743.859
          84.751 741.247C90.7638 738.636 116.694 717.152 128.908 706.736C139.242
          725.235 161.321 761.208 166.958 757.104C172.595 753 187.47 726.79
          194.203 714.198C218.63 760.213 271.336 813.628 286.744 786.019C302.152
          758.41 295.086 739.693 288.666 714.198C242.161 550.035 12.9221 653.103
          19.4986 651.238C26.0751 649.372 48.5801 670.825 48.5801
          673.157C48.5801 675.023 23.5267 686.06 11 691.346Z"
          fill="#A56B46" />
        <path
          d="M11 691.346C12.7224 694.455 16.4491 717.742 17.5765 786.019C38.2456
          791.616 51.2421 742.957 55.1567 717.929C62.5161 726.79 78.7382 743.859
          84.751 741.247C90.7638 738.636 116.694 717.152 128.908 706.736C139.242
          725.235 161.321 761.208 166.958 757.104C172.595 753 187.47 726.79
          194.203 714.198C218.63 760.213 271.336 813.628 286.744 786.019C302.152
          758.41 295.086 739.693 288.666 714.198C242.161 550.035 12.9221 653.103
          19.4986 651.238C26.0751 649.372 48.5801 670.825 48.5801
          673.157C48.5801 675.023 23.5267 686.06 11 691.346Z"
          stroke="black"
          stroke-width="9" />
      </g>
      <g id="Vector 2.13" filter="url(#filter2_d)">
        <path
          d="M145.031 776.659C133.306 771.381 99.9455 763.992 60.3048
          776.659C56.6343 775.106 60.3048 817.95 63.9752 821.986C67.6456 826.022
          139.525 824.47 142.89 820.434C146.254 816.398 150.231 787.214 149.007
          781.937C148.028 777.714 145.948 776.659 145.031 776.659Z"
          fill="#D3D3D3" />
        <path
          d="M145.031 776.659C133.306 771.381 99.9455 763.992 60.3048
          776.659C56.6343 775.106 60.3048 817.95 63.9752 821.986C67.6456 826.022
          139.525 824.47 142.89 820.434C146.254 816.398 150.231 787.214 149.007
          781.937C148.028 777.714 145.948 776.659 145.031 776.659Z"
          stroke="black"
          stroke-width="7" />
      </g>
      <g id="Vector 3.13" filter="url(#filter3_d)">
        <path
          d="M80.9701 802.132C90.0531 791.543 99.7174 789.149 108.181
          790.523C117.032 791.959 124.57 797.517 128.755 802.132"
          stroke="#4D6EE6"
          stroke-width="7" />
      </g>
      <g id="Vector 2.14" filter="url(#filter4_d)">
        <path
          d="M257.666 776.659C245.941 771.381 212.58 763.992 172.94
          776.659C169.269 775.106 172.94 817.95 176.61 821.986C180.28 826.022
          252.16 824.47 255.524 820.434C258.889 816.398 262.865 787.214 261.642
          781.937C260.663 777.714 258.583 776.659 257.666 776.659Z"
          fill="#D3D3D3" />
        <path
          d="M257.666 776.659C245.941 771.381 212.58 763.992 172.94
          776.659C169.269 775.106 172.94 817.95 176.61 821.986C180.28 826.022
          252.16 824.47 255.524 820.434C258.889 816.398 262.865 787.214 261.642
          781.937C260.663 777.714 258.583 776.659 257.666 776.659Z"
          stroke="black"
          stroke-width="7" />
      </g>
      <g id="Vector 3.14" filter="url(#filter5_d)">
        <path
          d="M193.605 802.132C202.688 791.543 212.352 789.149 220.815
          790.523C229.667 791.959 237.205 797.517 241.389 802.132"
          stroke="#4D6EE6"
          stroke-width="7" />
      </g>
      <g id="Vector 4.5" filter="url(#filter6_d)">
        <path
          d="M149.234 800.423C159.473 784.949 168.29 793.976 171.419 800.423"
          stroke="black"
          stroke-width="7" />
      </g>
      <g id="Vector 6.3" filter="url(#filter7_d)">
        <path
          d="M149.234 848.269C160.016 826.606 166.241 839.243 168.006 848.269"
          stroke="black"
          stroke-width="4" />
      </g>
      <path
        id="Vector 7.6"
        d="M236.269 891.336C202.687 859.237 148.863 829.112 77.5569
        891.336L88.5978 896.314C149.691 844.036 206.214 875.424 227.989
        897.824L236.269 891.336Z"
        fill="#D7A97F" />
      <path
        id="Vector 8.2"
        d="M58.7844 796.569C42.5234 793.045 30.3922 797.67 26.3593 800.423"
        stroke="black"
        stroke-width="7" />
      <path
        id="Vector 9.3"
        d="M258.455 803.707C274.19 799.648 284.353 804.383 287.467 807.258"
        stroke="black"
        stroke-width="7" />
      <g id="Vector 5.4" filter="url(#filter8_d)">
        <path
          d="M128.755 882.445C153.612 901.014 175.519 890.182 183.365 882.445"
          stroke="black"
          stroke-width="4" />
      </g>
    </g>
    <g id="bub1">
      <circle
        in:draw={{ duration: du, delay: bub1, easing: linear }}
        id="Ellipse 1"
        cx="328.5"
        cy="601.5"
        r="43.5"
        stroke="black"
        stroke-width="12" />
    </g>
    <g id="bubble">
      <path
        in:draw={{ duration: 3000, delay: bubble, easing: linear }}
        id="Union"
        d="M986.415 167.869L985.418 172.666L989.92 174.602C1028.45 191.168 1052
        218.759 1052 248.505C1052 281.963 1022.09 312.753 975.003
        328.003L971.078 329.274L970.86 333.394C968.406 379.767 919.991 418.745
        857.978 418.745C854.49 418.745 851.039 418.62 847.633 418.376L844.071
        418.12L842.148 421.129C821.632 453.235 771.784 477 712.106 477C661.244
        477 617.276 459.692 592.762 434.51L591.065 432.766L588.633
        432.697C526.877 430.946 479.775 390.626 479.775 343.631C479.775 341.844
        479.841 340.072 479.973 338.313L480.354 333.213L475.379 332.029C420.312
        318.923 384 285.307 384 248.505C384 221.183 403.817 195.713 437.005
        178.848L441.135 176.749L440.149 172.222C439.077 167.299 438.518 162.236
        438.518 157.067C438.518 109.028 487.779 67.942 551.499 67.942C558.679
        67.942 565.698 68.4713 572.498 69.4818L576.657 70.0999L578.657
        66.4014C597.226 32.0691 648.824 6 711.369 6C772.284 6 822.898 30.7474
        842.612 63.8164L844.755 67.4097L848.867 66.6421C857.226 65.082 865.949
        64.255 874.923 64.255C938.643 64.255 987.905 105.341 987.905
        153.38C987.905 158.316 987.395 163.155 986.415 167.869Z"
        stroke="black"
        stroke-width="12" />
    </g>
    <g id="kid" in:fade={{ duration: du, delay: kid }}>
      <path
        id="Ellipse 3"
        d="M918.349 295.312C918.349 328.3 906.655 349.003 888.497 361.798C869.87
        374.925 843.355 380.5 812.517 380.5C782.121 380.5 754.481 372.945
        734.627 357.665C715.038 342.59 702.357 319.507 702.357 286.672C702.357
        253.421 715.392 216.852 736.099 188.644C756.899 160.309 784.342 141.786
        812.517 141.786C840.287 141.786 866.639 161.984 886.528 192.611C906.267
        223.008 918.349 261.862 918.349 295.312Z"
        fill="#FFD6D6"
        stroke="#EED9D9"
        stroke-width="15" />
      <path
        id="Subtract"
        d="M859.903 127.56C854.353 125.412 848.267 124.3 841.911 124.461C817.058
        125.09 797.264 144.987 797.874 169.063C798.007 174.341 799.114 179.377
        801.024 184.015C801.887 186.11 801.503 188.671 800.373 190.394C799.821
        191.236 799.17 191.755 798.552 191.979C797.986 192.185 797.296 192.201
        796.436 191.759C780.545 183.605 769.685 167.994 769.227 149.892C768.542
        122.843 791.391 100.109 820.54 99.3708C840.154 98.874 857.465 108.491
        866.867 123.088C867.403 123.92 867.435 124.573 867.302 125.078C867.155
        125.633 866.739 126.248 865.991 126.794C864.459 127.913 862.02 128.379
        859.903 127.56Z"
        fill="#F8C544"
        stroke="#D3BE88"
        stroke-width="4" />
      <g id="Component 1">
        <ellipse
          id="Ellipse 4"
          cx="775.931"
          cy="261.143"
          rx="24.005"
          ry="36.2449"
          fill="#0959D1" />
        <ellipse
          id="Ellipse 5"
          cx="780.984"
          cy="248.078"
          rx="12.2131"
          ry="13.065"
          fill="#F8F8F8" />
      </g>
      <g id="Component 2">
        <ellipse
          id="Ellipse 4_2"
          cx="775.931"
          cy="261.143"
          rx="24.005"
          ry="36.2449"
          fill="#0959D1" />
        <ellipse
          id="Ellipse 5_2"
          cx="780.984"
          cy="248.078"
          rx="12.2131"
          ry="13.065"
          fill="#F8F8F8" />
      </g>
      <g id="Component 3">
        <ellipse
          id="Ellipse 4_3"
          cx="853.834"
          cy="261.143"
          rx="24.005"
          ry="36.2449"
          fill="#0959D1" />
        <ellipse
          id="Ellipse 5_3"
          cx="858.887"
          cy="248.078"
          rx="12.2131"
          ry="13.065"
          fill="#F8F8F8" />
      </g>
      <g id="Component 4">
        <ellipse
          id="Ellipse 4_4"
          cx="853.834"
          cy="261.143"
          rx="24.005"
          ry="36.2449"
          fill="#0959D1" />
        <ellipse
          id="Ellipse 5_4"
          cx="858.887"
          cy="248.078"
          rx="12.2131"
          ry="13.065"
          fill="#F8F8F8" />
      </g>
      <path
        id="Vector 10"
        d="M780.007 334.31C805.093 362.208 830.921 345.934 840.699 334.31"
        stroke="#DBCCCC"
        stroke-width="8" />
      <path
        id="Polygon 1"
        d="M810.426 324.923C810.104 325.123 809.696 325.123 809.374
        324.923L801.908 320.303C801.051 319.773 801.427 318.453 802.434
        318.453L817.366 318.453C818.373 318.453 818.749 319.773 817.893
        320.303L810.426 324.923Z"
        fill="#DBCCCC" />
      <ellipse
        id="Ellipse 6"
        rx="21.1866"
        ry="27.9992"
        transform="matrix(0.810286 -0.586035 0.585804 0.810453 688.569 275.181)"
        fill="#FFD6D6" />
      <path
        id="Subtract_2"
        d="M689.581 257.379C690.819 257.889 689.312 259.811 687.973
        259.811V259.811C681.942 259.811 677.053 264.926 677.053 271.236C677.053
        276.304 680.207 280.602 684.574 282.097C684.868 282.197 684.834 282.661
        684.525 282.661V282.661C677.224 282.661 671.305 276.779 671.305
        269.522C671.305 262.266 677.224 256.383 684.525 256.383C686.316 256.383
        688.024 256.737 689.581 257.379Z"
        fill="#EED9D9" />
      <ellipse
        id="Ellipse 7"
        rx="21.1866"
        ry="27.9992"
        transform="matrix(0.810286 -0.586035 0.585804 0.810453 688.569 275.181)"
        fill="#FFD6D6" />
      <path
        id="Subtract_3"
        d="M689.581 257.379C690.819 257.889 689.312 259.811 687.973
        259.811V259.811C681.942 259.811 677.053 264.926 677.053 271.236C677.053
        276.304 680.207 280.602 684.574 282.097C684.868 282.197 684.834 282.661
        684.525 282.661V282.661C677.224 282.661 671.305 276.779 671.305
        269.522C671.305 262.266 677.224 256.383 684.525 256.383C686.316 256.383
        688.024 256.737 689.581 257.379Z"
        fill="#EED9D9" />
      <ellipse
        id="Ellipse 8"
        rx="21.1866"
        ry="27.9992"
        transform="matrix(-0.810286 -0.586035 -0.585804 0.810453 930.431
        275.181)"
        fill="#FFD6D6" />
      <path
        id="Subtract_4"
        d="M929.419 257.379C928.181 257.889 929.688 259.811 931.027
        259.811V259.811C937.058 259.811 941.947 264.926 941.947 271.236C941.947
        276.304 938.793 280.602 934.426 282.097C934.132 282.197 934.166 282.661
        934.475 282.661V282.661C941.776 282.661 947.695 276.779 947.695
        269.522C947.695 262.266 941.776 256.383 934.475 256.383C932.684 256.383
        930.976 256.737 929.419 257.379Z"
        fill="#EED9D9" />
      <ellipse
        id="Ellipse 9"
        rx="21.1866"
        ry="27.9992"
        transform="matrix(-0.810286 -0.586035 -0.585804 0.810453 930.431
        275.181)"
        fill="#FFD6D6" />
      <path
        id="Subtract_5"
        d="M929.419 257.379C928.181 257.889 929.688 259.811 931.027
        259.811V259.811C937.058 259.811 941.947 264.926 941.947 271.236C941.947
        276.304 938.793 280.602 934.426 282.097C934.132 282.197 934.166 282.661
        934.475 282.661V282.661C941.776 282.661 947.695 276.779 947.695
        269.522C947.695 262.266 941.776 256.383 934.475 256.383C932.684 256.383
        930.976 256.737 929.419 257.379Z"
        fill="#EED9D9" />
      <rect
        id="Rectangle 1"
        width="50.7285"
        height="10.8733"
        rx="4"
        transform="matrix(0.969508 0.245059 -0.244921 0.969543 836.115 200.204)"
        fill="#F8C544" />
      <rect
        id="Rectangle 2"
        width="50.7286"
        height="10.8732"
        rx="4"
        transform="matrix(0.965906 -0.258892 0.258747 0.965945 745.585 212.431)"
        fill="#F8C544" />
    </g>
    <g
      id="gear"
      in:fade={{ duration: du, delay: gear }}
      on:introend={() => (startAnim = true)}
      class:startAnim>
      >
      <path
        id="Vector_2"
        d="M629.207 226.601L643.926 235.082C645.607 236.05 646.387 238.053
        645.812 239.903C641.988 252.191 635.46 263.292 626.922 272.512C626.283
        273.203 625.428 273.656 624.497 273.797C623.566 273.938 622.615 273.759
        621.799 273.289L607.091 264.81C600.903 270.103 593.788 274.209 586.105
        276.921V293.877C586.105 294.818 585.784 295.73 585.196 296.464C584.607
        297.199 583.785 297.711 582.866 297.917C570.793 300.623 557.825 300.763
        545.142 297.92C543.246 297.494 541.895 295.818 541.895
        293.878V276.921C534.212 274.209 527.097 270.103 520.909 264.81L506.2
        273.289C505.385 273.759 504.433 273.938 503.502 273.797C502.571 273.656
        501.716 273.203 501.077 272.512C492.54 263.292 486.012 252.191 482.188
        239.903C481.612 238.053 482.392 236.05 484.073 235.082L498.793
        226.601C497.315 218.601 497.315 210.399 498.793 202.399L484.074
        193.919C482.393 192.95 481.613 190.948 482.188 189.097C486.012 176.809
        492.54 165.708 501.078 156.488C501.717 155.798 502.572 155.345 503.503
        155.203C504.434 155.062 505.385 155.241 506.201 155.711L520.909
        164.19C527.097 158.898 534.212 154.792 541.895 152.079V135.123C541.895
        134.182 542.216 133.27 542.804 132.536C543.393 131.801 544.215 131.289
        545.134 131.083C557.207 128.377 570.175 128.237 582.858 131.08C584.754
        131.506 586.105 133.182 586.105 135.122V152.079C593.788 154.791 600.903
        158.897 607.091 164.19L621.8 155.711C622.615 155.241 623.567 155.062
        624.498 155.203C625.429 155.344 626.284 155.797 626.923 156.488C635.46
        165.708 641.989 176.809 645.812 189.097C646.388 190.947 645.608 192.95
        643.927 193.918L629.207 202.399C630.685 210.399 630.685 218.601 629.207
        226.601V226.601ZM591.632 214.5C591.632 199.292 579.236 186.919 564
        186.919C548.764 186.919 536.368 199.292 536.368 214.5C536.368 229.708
        548.764 242.081 564 242.081C579.236 242.081 591.632 229.708 591.632
        214.5Z"
        fill="#37B562" />
    </g>
  </g>
  <defs>
    <filter
      id="filter0_d"
      x="18.9462"
      y="653.467"
      width="277.641"
      height="286.533"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB">
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" />
      <feOffset dy="4" />
      <feGaussianBlur stdDeviation="2" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow" />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow"
        result="shape" />
    </filter>
    <filter
      id="filter1_d"
      x="0.637207"
      y="616.5"
      width="303.863"
      height="189.588"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB">
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" />
      <feOffset dy="4" />
      <feGaussianBlur stdDeviation="2" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow" />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow"
        result="shape" />
    </filter>
    <filter
      id="filter2_d"
      x="51.2844"
      y="766.165"
      width="105.449"
      height="69.6813"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB">
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" />
      <feOffset dy="4" />
      <feGaussianBlur stdDeviation="2" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow" />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow"
        result="shape" />
    </filter>
    <filter
      id="filter3_d"
      x="74.3136"
      y="786.67"
      width="61.0337"
      height="25.8127"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB">
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" />
      <feOffset dy="4" />
      <feGaussianBlur stdDeviation="2" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow" />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow"
        result="shape" />
    </filter>
    <filter
      id="filter4_d"
      x="163.919"
      y="766.165"
      width="105.449"
      height="69.6813"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB">
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" />
      <feOffset dy="4" />
      <feGaussianBlur stdDeviation="2" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow" />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow"
        result="shape" />
    </filter>
    <filter
      id="filter5_d"
      x="186.948"
      y="786.67"
      width="61.0337"
      height="25.8127"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB">
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" />
      <feOffset dy="4" />
      <feGaussianBlur stdDeviation="2" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow" />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow"
        result="shape" />
    </filter>
    <filter
      id="filter6_d"
      x="142.315"
      y="788.379"
      width="36.2533"
      height="21.9754"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB">
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" />
      <feOffset dy="4" />
      <feGaussianBlur stdDeviation="2" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow" />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow"
        result="shape" />
    </filter>
    <filter
      id="filter7_d"
      x="143.443"
      y="834.308"
      width="30.5258"
      height="22.8527"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB">
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" />
      <feOffset dy="4" />
      <feGaussianBlur stdDeviation="2" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow" />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow"
        result="shape" />
    </filter>
    <filter
      id="filter8_d"
      x="123.558"
      y="880.843"
      width="65.212"
      height="21.8591"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB">
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" />
      <feOffset dy="4" />
      <feGaussianBlur stdDeviation="2" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0" />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow" />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow"
        result="shape" />
    </filter>
  </defs>
</svg>
