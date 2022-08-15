<template>
  <div>
    <h1 v-if="error.statusCode === 404">Page Not Found</h1>
    <h1 v-else>An Error Occurred</h1>
    <nuxt-link to="/">Click to visit Home page</nuxt-link>
  </div>
</template>

<script>
export default {
  props: {
    error: {
      type: [Object, Error],
      default: () => {},
    },
  },
}
</script>
