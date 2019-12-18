<template lang="html">
  <div>
    <ul>
      <country-item v-for="(country, index) in countries" v-bind:country="country" v-bind:key="index"></country-item>
    </ul>
  </div>
</template>

<script>
import CountryItem from './CountryItem.vue';

export default {
  name: 'countries-list',
  props: ['countries'],
  components: {
    "country-item" : CountryItem
  }
}
</script>

<style lang="css" scoped>

</style>
