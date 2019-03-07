<template>
  <div class="row">
    <app-quote 
      v-for="(quote, index) in quotes"
      v-bind:key="quote"
      @click.native="removeQuote(index)"
    >
      {{ quote }}
    </app-quote>
  </div>
</template>

<script>
import Quote from './Quote.vue'
export default {
  props: ['quotes'],
  components: {
    appQuote: Quote
  },
  methods: {
    removeQuote(index){
      this.$emit('removeQuote', index)
    }
  }
}
</script>

<style>

</style>
