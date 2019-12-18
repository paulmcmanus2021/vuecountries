<template lang="html">
  <div>
    <label for="country-dropdown">Choose a Country:</label>

    <select v-on:change="handleChange" name="country-dropdown" v-model="countryChoice">
      <option v-for="(country, index) in countries" :key="index" :value="country">
        {{ country.name }}
      </option>

    </select>

  </div>
</template>

<script>
import { eventBus } from '../main.js'
export default {
  name: "country-dropdown",
  data(){
    return {
      countryChoice: null
    }
  },
  props: ["countries"],
  methods: {
    handleChange : function (){
      eventBus.$emit('country-selected', this.countryChoice)

    }
  }
}
</script>

<style lang="css" scoped>
</style>
