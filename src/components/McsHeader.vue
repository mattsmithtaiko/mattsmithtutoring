<template>
  <div>
    <div class="text-h2 font-weight-bold text-center pt-4">
      <slot></slot>
    </div>
    <div class="text-h6 text-center pb-2" v-if="subheader">
      {{ subheader }}
    </div>
    <div class="pb-4" v-else></div>
  </div>
</template>

<script>
export default {
  props: {
    subheader: String
  }
}
</script>
