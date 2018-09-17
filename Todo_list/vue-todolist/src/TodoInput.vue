<script>
  export default{
    data(){
      return {
        text:'',
      };
    },
    methods:{
      inputsubmit(){
        this.$emit('submit',this.text);
        this.text='';
      },
    }
  }
</script>

<template>
  <form @submit.prevent="inputsubmit">
    <input type="text" v-model="text"/>
    <button type="submit">Submit</button>
  </form>
</template>