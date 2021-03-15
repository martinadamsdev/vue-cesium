<script lang="ts">
import Vue from 'vue';
import VViewer from "@/components/v-viewer/index.vue";
// Uncomment import and local "components" registration if library is not registered globally.
// import { VueCesiumSample } from '@/entry.esm';

export default Vue.extend({
  name: 'ServeDev',
  components: {VViewer},
});
</script>

<template>
  <div id="app">
    <v-viewer />
  </div>
</template>
