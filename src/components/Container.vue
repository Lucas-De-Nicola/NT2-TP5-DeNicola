<template>

  <section class="src-components-container">
    <div class="square" :style="{background: color}" @click="squareSelected">
	  </div>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-container',
    props: ['color'],
    mounted () {

    },
    data () {
      return {

      }
    },
    methods: {
      squareSelected(){
         this.$emit('squareSelected', this.color);
      }
    },
    computed: {

    }
}


</script>

<style scoped lang="css">
  .src-components-container {
    margin: 20px auto;
	  max-width: 600px;
  }

  .square{
    width: 30%;
	  background: blue;
	  padding-bottom: 30%;
	  float: left;
	  margin: 1.66%;
	  border-radius: 10%;
	  transition: background 0.8s;
	  -webkit-transition: background 0.8s;
	  -moz-transition: background 0.8s;
  }
</style>
