<template>
  <v-card>
    <v-card-title primary-title>
      <div>
        <h3 class="headline search__heading">Would you like to detect language?</h3>
        <v-textarea
          box
          name="input-7-4"
          rows="6"
          label="Write down the phrase"
          value=""
          color="#FC7753"
          class="search__textarea"
          v-model="message"
        ></v-textarea>
      </div>
    </v-card-title>

    <v-card-actions>
      <router-link v-bind:to="`/${encodeURIComponent(message)}`" class="button__link">
        <v-btn flat color="#FC7753">Detect</v-btn>
      </router-link>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      message: '',
    }
  }
}
</script>

<style>
  .search__heading {
    margin-bottom: 20px;
  }
  .button__link {
    text-decoration: none;
  }
</style>
