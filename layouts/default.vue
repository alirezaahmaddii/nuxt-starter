<template>
  <div>

    <!--  drawer  -->
    <site-drawer />

    <!--  content page  -->
    <Nuxt/>

  </div>
</template>

<script>
import SiteDrawer from "~/layouts/site-drawer";
export default {
  name: "default",
  components: {SiteDrawer}
}
</script>

<style scoped>

</style>
