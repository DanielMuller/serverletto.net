<template lang="pug">
.item
  .polaroid
    img(:src="image" )
    .caption
      slot {{ caption }}
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PolaroidImage',
  props: {
    caption: {
      type: String,
      required: false,
    },
    image: {
      type: String,
      required: true,
    },
  },
});
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap');
.polaroid {
  background: #fff;
  padding: 1rem;
  box-shadow: 0 0.2rem 1.2rem rgba(0, 0, 0, 0.2);
  text-align: center;
}
.polaroid > img {
  max-width: 100%;
  height: auto;
}
.caption {
  font-size: 1.8rem;
  text-align: center;
  font-family: 'Permanent Marker', cursive;
}
.item {
  width: 40vh;
  display: inline-block;
  margin-top: 2rem;
  transform: scale(0.6, 0.6);
}
.item .polaroid:before {
  content: '';
  position: absolute;
  z-index: -1;
}
</style>
