<template>
  <div class="row">
    <form>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
          
          <textarea class="form-control" v-model="quote" rows="3"></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group"
          :style="{display: 'flex', justifyContent: 'center'}">
        <button @click.prevent="createNew" class="btn btn-primary">Add Quote</button>
      </div>
     </form>
  </div>
  
</template>

<script>
  export default {
    data: function(){
      return {
        quote: ''
      }
    },
    methods: {
      createNew() {
        this.$emit('quoteAdded', this.quote)
        this.quote = ''
      }
    }
  }
</script>

<style scoped>

</style>
