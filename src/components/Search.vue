<template>
  <div class="col s12">
    <form class="col s12" @submit.prevent>
      <div class="input-field">
        <i class="material-icons prefix">search</i>
        <input id="search"
               v-model="query"
               @input="onInput"
               type="text">
        <label class="active" for="search">Search</label>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  props: {
    value: String
  },
  computed: {
    query () { return this.value }
  },
  methods: {
    onInput (event) {
      this.$emit('input', event.target.value)
    }
  }
}
</script>
