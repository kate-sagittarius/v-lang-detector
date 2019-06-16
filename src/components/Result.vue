<template>
  <v-card>
    <v-card-title primary-title>
      <div>
        <h3 class="headline result__heading">The phrase is probably written in…</h3>
      </div>
    </v-card-title>
      <div class="result-wrapper" v-if="results[0]">
        <div class="result__lang">{{ results[0].language_name }}</div>
        <div class="result__accuracy">Accuracy: {{ results[0].percentage }}</div>
      </div>
      <div v-else class="result-wrapper progress">
        <v-progress-circular
          indeterminate
          color="#000000"
        ></v-progress-circular>
      </div>
  </v-card>
</template>

<script>
import axios from 'axios';

const apiParams = (query) => {
  const apiURL = 'http://api.languagelayer.com/detect';
  const key = '2695c6ed637b6ce743d4164c096cd0f7';

  return `${apiURL}?access_key=${key}&query=${encodeURIComponent(query)}`;
};

export default {
  data () {
    return {
      results: []
    }
  },

  mounted () {
    axios
      .get(apiParams(this.$route.params.phrase))
      .then(response => {
        this.results = response.data.results;
      })   
  },

  watch: {
    '$route.params.phrase' () {
      axios
        .get(apiParams(this.$route.params.phrase))
        .then(response => {
          this.results = response.data.results;
        })   
    }
  }

}
</script>

<style>
  .result__heading {
    margin-bottom: 20px;
  }
  .result-wrapper {
    padding: 24px 16px 16px;
    height: 228px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
  }
  .progress {
    padding-top: 56px;
  }
  .result__lang {
    font-size: 28px;
    margin-top: 16px;
  }
  .result__accuracy {
    align-self: flex-start;
    color: #FC7753;
    text-transform: uppercase;
    font-size: 14px;
    font-weight: 500;
    margin-left: 10px;
  }
</style>