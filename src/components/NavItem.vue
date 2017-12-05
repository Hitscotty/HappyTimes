<template>
  <router-link :to="NavData.link" class="item"> {{NavData.title }}</router-link>
</template>
<script>
export default {
  name: "NavItem",
  props: {
    NavData: {
      type: Object,
      default: () => ({
        title: "default",
        link: "/"
      })
    }
  }
};
</script>
