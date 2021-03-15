<template>
  <div id="v-viewer">
    <slot name="v-viewer-container">
      <div id="v-viewer-container"></div>
    </slot>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import * as Cesium from 'cesium'
declare global {
  interface Window {
    viewer: Object
  }
}

// interface Props {
//   counter: number;
//   initCounter: number;
//   message: {
//     action: string | null;
//     amount: number | null;
//   };
// }

export default Vue.extend({
  name: 'VViewer', // vue component name
  props: {

  },
  mounted() {
    window.viewer = new Cesium.Viewer('v-viewer-container', {});
  },
  computed: {

  },
  methods: {
    // increment(arg: Event | number): void {
    //
    // },
    // decrement(arg: Event | number): void {
    //
    // },
    // reset(): void {
    // },
  },
});
</script>

<style scoped>
@import "~cesium/Build/Cesium/Widgets/widgets.css";
#v-viewer, #v-viewer-container {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  overflow: hidden;
}
</style>