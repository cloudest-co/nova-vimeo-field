<template>
  <PanelItem :field="field">
    <template v-slot:value>
      <iframe
          v-if="field.value"
          ref="player"
          :src="videoUrl"
          :height="height"
          :width="width"
          frameborder="0"
          webkitallowfullscreen
          mozallowfullscreen
          allowfullscreen
      >
      </iframe>
      <div v-else>No URL entered</div>
    </template>
  </PanelItem>
</template>

<script>
export default {
  props: ['index', 'resource', 'resourceName', 'resourceId', 'field'],

  computed: {
    videoUrl() {
      return this.field.value;
    },
    height() {
      return this.field.options.height;
    },
    width() {
      return this.field.options.width;
    },
  },
}
</script>
