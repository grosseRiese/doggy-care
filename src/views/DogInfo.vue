<template>
    <section id="doginfo">
      <img :src="dog.img" :alt="dog.name">
      <h1> {{dog.name}}</h1>
       <section class="section-info">
            <p><b>Breed: </b> <i>{{dog.breed}}</i></p>        
            <p><b>Age: </b>{{dog.age}}y</p>        
            <p><b>Chip Number: </b>{{dog.chipNumber}}</p>
            <p><b>Owner:</b> {{ dog.owner.name }} {{ dog.owner.lastName }}</p>
            <p>Phone: {{dog.owner.phoneNumber}}</p>
        </section>
    </section>
</template>

<script>
export default {
  name:'DogInfo',
  props:{
    dogs: Array
  },
  computed:{
    dog(){
      return this.dogs.filter(dog => dog.chipNumber === this.$route.params.chipNumber)[0];
    }
  }
}
</script>

<style lang="scss">

#doginfo{
    box-shadow:5px 8px 16px 5px rgba(0,0,0,0.2);
    width:45%;
   /* margin-left: 25%;
    margin-right: 25%; */
    margin: auto;
    text-align: center;
    font-size:2vw;
    background-color: rgba(238, 190, 190, 0.479);
    transition: 0.3s;
     

        img {
          width:100%;
          max-width: 100%;
          min-width: 100%;
        
        }
      
    
      p{
        color:rgb(128, 111, 111);
      }

      &:hover {
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
      }
      .section-info{
       clip-path: polygon(0% 0%, 100% 0%, 100% 75%, 75% 75%, 75% 100%, 50% 75%, 0% 75%);
        padding-bottom: 6rem;
        padding-top: 1rem;
        background-color: rgba(238, 190, 190, 0.479);
      }
  }
</style>