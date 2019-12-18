<template lang="html">
  <li>
    {{country.name}}
  </li>
</template>

<script>
export default {
  name: 'country-item',
  props: ['country']
}
</script>

<style lang="css" scoped>
</style>
