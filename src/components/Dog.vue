<template>
  <article class="dog" @click="goTo" >
      <img :src="dog.img" alt="a dog" />
      <h2>{{dog.name}}</h2>
      <h4>{{dog.breed}}</h4>
  </article>
</template>

<script>
export default {
name:'Dog',
props:{
  dog: Object
},
methods:{
  goTo(){
    this.$router.push('/dogs/' + this.dog.chipNumber);
  }
}
}
</script>

<style lang="scss">
    .dog {
        background: white;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 3rem 0;
        border-radius: 3px;
        box-shadow: 0 0 1rem rgba(0,0,0,.1);
        transition: all .2s ease;
        filter: grayscale(1);
        border-top: 3.5rem solid rgb(105, 204, 138);
        
        &:hover {
            transform: scale(1.1);
            box-shadow: 0 0 1.5rem rgba(0,0,0,.05);
            filter: grayscale(0);
            cursor: pointer;
        }
        img {
            width: 8rem;
            height: 8rem;
            object-fit: cover;
            border-radius: 9999rem;
            margin: 0 0 1rem 0;
        }
        h2 {
            margin: 0;
            padding: 0;
            font-size: 1.6rem;
        }
        h4 {
            margin: 0;
            padding:0;
            font-weight: 400;
            opacity: .6;
            color:rgba(146, 148, 16, 0.959);
        }
    }
</style>