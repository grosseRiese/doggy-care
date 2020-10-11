<template>
<section id="dogs">
  <h2>Our Dogs</h2>
  <Dog v-for="dog in dogs" :key="dog.chipNumber" :dog="dog" />
</section>
</template>

<script>

import Dog from '@/components/Dog.vue';

export default {
  name: 'Dogs',
   props: {
    dogs: Array
  },
  components:{
    Dog
  }
}
</script>
<style lang="scss">


   #dogs {
        max-width: 100%;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 1.3rem;
        background-color: rgba(207, 248, 239, 0.514);

        h2 {
            grid-column: auto / span 4;
            text-align: center;
             text-transform: uppercase;
             color:rgb(69, 163, 14);
        }
        
    }

</style>