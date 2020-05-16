<template>
  <svg :width="getWidth" :height="getHeight" x="0.0" y="0.0" viewBox="0 0 137 137">
  <defs>
    <filter id="a" x="9" y="0" width="154" height="182" filterUnits="userSpaceOnUse">
      <feOffset dy="15" input="SourceAlpha"/>
      <feGaussianBlur stdDeviation="15" result="b"/>
      <feFlood flood-opacity="0.169"/>
      <feComposite operator="in" in2="b"/>
      <feComposite in="SourceGraphic"/>
      </filter>
  </defs>
  <g>
    <rect class="a" width="100%" height="100%" rx="48"/>
    <g class="c" transform="matrix(1, 0, 0, 1, 0, -8)">
      <rect class="b" width="64" height="92" rx="23" transform="translate(54 30)"/>
      </g>
    </g>
  </svg>
</template>

<script>
export default {
  props: {
    width: {
      type: Number,
      default: 40
    }
  },

  computed: {
    getWidth() {
      return this.width;
    },

    getHeight() {
      return Math.ceil((this.getWidth / 48) * 48);
    }
  }
};
</script>

<style>
.a{fill:#f7f7f7;}
.b{fill:#6edceb;}
.c{filter:url(#a);}
</style>

