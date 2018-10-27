<template>
  <div>
    <navigation class="mb-5"/>
    <b-container>
      <nuxt/>
    </b-container>
    <bottomfooter class="mt-5"/>
  </div>
</template>
<script>
  import navigation from "~/components/layout/navigation";
  import bottomfooter from "~/components/layout/footer";

  export default {
    components: {
      navigation, bottomfooter
    }
  }
</script>
<style lang="scss">
</style>
