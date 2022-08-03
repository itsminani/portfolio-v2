<template>
  <v-vanta effect="dots" :options=options></v-vanta>
</template>
 
<script lang="ts">
  import VVanta from 'vue-vanta';
  export default {
    components: { VVanta },
    data () {
      return {
        options: {
            mouseControls: true,
            touchControls: true,
            gyroControls: false,
            minHeight: 200.00,
            minWidth: 200.00,
            scale: 1.00,
            scaleMobile: 1.00
        }
      }
    }
  }
</script>