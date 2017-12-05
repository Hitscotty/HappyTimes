<template>
  <a class="item" v-bind:href="NavData.link">
    {{NavData.title}}
  </a>
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
  }

</script>
