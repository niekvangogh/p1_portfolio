<template>
  <div>
    <navigation/>
    <b-container>
      <nuxt/>
    </b-container>
  </div>
</template>
<script>
  import navigation from "~/components/layout/navigation";

  export default {
    components: {
      navigation
    }
  }
</script>
<style lang="scss">
  nav {
    margin-bottom: 5rem;
  }
</style>
