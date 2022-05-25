<template>
  <div>
    <h2>Filter LearnVue Articles</h2>
    <InputText type="text" v-model="query" />

    <search-results :query="query" />
    
    <Button @click="reset" label="Reset" class="p-button-outlined p-button-warning" />


  </div>
</template>


<script>
import { ref } from "vue";
import SearchResults from "./SearchResults.vue";
import Button from "primevue/button";

export default {
  components: {
    SearchResults,
    Button,
  },
  setup() {
    const query = ref("");

    const reset = (evt) => {
      query.value = ""; // clears the query
    };

    return {
      reset,
      query,
    };
  },
};
</script>
