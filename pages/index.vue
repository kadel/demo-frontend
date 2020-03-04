<template>
  <v-container>
    <v-layout column align-center>
      <v-form @submit.prevent="onSubmit">
        <v-text-field v-model="name" placeholder="Name" />
        <v-btn @click="onSubmit">Greet</v-btn>
      </v-form>
      Greeting: {{ greeting }}
      <br />
      Counter: {{ counter }}
    </v-layout>
  </v-container>
</template>

<script>
export default {
  components: {},

  data() {
    return {
      name: '',
      greeting: '',
      counter: ''
    }
  },
  async mounted() {},
  methods: {
    async onSubmit() {
      const data = await this.$axios.$get('/api/hello', {
        params: { name: this.name }
      })
      this.greeting = data.content
      this.counter = data.id
    }
  }
}
</script>
