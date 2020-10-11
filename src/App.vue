<template>
  <div id="app">
    <nav id="nav">
      <router-link to="/" class="nav-route">Home  </router-link> <span class="nav-route"> |</span>
      <router-link to="/dogs" class="nav-route">Dogs</router-link>
    </nav>
    <router-view :dogs="dogs"/>
  </div>
</template>

<script>
import dogs from'@/assets/dogs.json';
export default{
  name:'App',
  data(){
    return{
      dogs:dogs
    }
  }
}
</script>

<style lang="scss">


  #app{
    max-width: 100%;
    margin: 1rem auto;

    #nav{
      background-color: rgba(170, 248, 216, 0.801);
      width: 100%;
      padding: 2.4rem;
      display: flex;
      margin-bottom: 3rem;
      
      flex-flow: row wrap;
      justify-content: center;
      list-style: none;
    }
    .nav-route{
      text-decoration: none;
      display: block;
      padding: 0 1.7em;
      color: darkgoldenrod;
      font-size: 2.4vw;
      font-weight: 900;
      
    }
  }

</style>
