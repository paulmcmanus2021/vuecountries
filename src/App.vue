<template>
  <div>
    <h1>Countries</h1>
    <div class="main-container">
      <countries-list v-bind:countries='countries'></countries-list>

    </div>
  </div>
</template>

<script>
import CountriesList from './components/CountriesList.vue';

export default {
  name: 'app',
  data(){
    return {
      countries: [],
    }
  },
  mounted(){
    fetch('https://restcountries.eu/rest/v2/all')
    .then(res => res.json())
    .then(countries => this.countries = countries)
  },

  components: {
    "countries-list": CountriesList
  }
}


</script>

<style>

</style>
