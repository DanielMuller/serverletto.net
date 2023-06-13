<template lang="pug">
q-page.column.items-center.justify-evenly
  h1 Past Events
  .q-gutter-md
    q-card.q-pa-md(style="width:80vw;max-width:800px")
      q-card-section(horizontal)
        q-card-section.col-5.flex.flex-center
          q-img.rounded-borders(src="/paris.png")
        q-card-section.q-pt-xs
          .text-overline 7th June 2023
          .text-h5.q-mt-sm.q-mb-xs Paris

    q-card.q-pa-md(style="width:80vw;max-width:800px")
      q-card-section(horizontal)
        q-card-section.col-5.flex.flex-center
          q-img.rounded-borders(src="~assets/serverlessguru-logo.png")
        q-card-section.q-pt-xs
          .text-overline 7th &amp; 8th June 2023
          .text-h5.q-mt-sm.q-mb-xs Washington DC

  polaroid-image(image="/serverlessguru-logo.svg")
    p From ServerlessGuru
    p with
    q-icon(name="favorite" style="color: #ff0000; font-size: 3em;")
</template>
<script>
import PolaroidImage from 'components/PolaroidImage.vue';
export default {
  name: 'IndexPage',
  components: {
    PolaroidImage,
  },
};
</script>
