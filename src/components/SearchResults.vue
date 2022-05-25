<template>
  <div class="root">
    <p>Showing results for "{{ query }}"</p>
  </div>
</template>
<script>

import { computed } from "vue";
export default {
  props: {
    query: String,
  },
};
</script>>