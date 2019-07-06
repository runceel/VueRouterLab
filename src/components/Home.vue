<template>
  <div>
    <h2>Home</h2>
    <router-link to="/about">About ページへ</router-link>

    <div>
      <input type="text" v-model="input" />
    </div>
    <div>
      <span>{{ output }}</span>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  data() {
    return {
      input: '',
      output: '',
    };
  },
  watch: {
    input(val: string) {
      this.output = val.toUpperCase();
    },
  },
});
</script>
