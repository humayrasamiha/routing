<template>
  <div class="view-profile">
    <h2>Profile for {{ user_id }}</h2>
  </div>
</template>

<script>
export default {
  name: "ViewProfile",
  data() {
    return {
      user_id: this.$route.params.user_id
    };
  },
  methods: {
    updateId() {
      this.user_id = this.$route.params.user_id;
    }
  },
  watch: {
    $route: "updateId"
  }
};
</script>

<style scoped>
</style>
