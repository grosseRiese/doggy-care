<template>
<section id="home">
<h1>Welcome to Doggy DayCare</h1>
   <b-carousel
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    indicators
    img-width="1024"
    img-height="480"
  >
  
    <b-carousel-slide
      caption="After playing"
      img-src='https://images.unsplash.com/photo-1504208434309-cb69f4fe52b0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1024&h=480&q=80'
    >
      <p> We currently takes  care of 
        <b>{{dogs.length}} </b><i> dog/'s.</i>
      </p>
    </b-carousel-slide>
    <b-carousel-slide
      caption="Eating time"
      img-src="https://images.unsplash.com/photo-1546975490-e8b92a360b24?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1024&h=480&q=80"
    ></b-carousel-slide>
    <b-carousel-slide
      caption="Reading hour"
      img-src="https://images.unsplash.com/photo-1535930891776-0c2dfb7fda1a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1024&h=480&q=80"
    ></b-carousel-slide>
  </b-carousel>
</section>
</template>

<script>

export default {
  name: 'Home',
  props:{
    dogs:Array
  }
}
</script>
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Architects+Daughter&family=Fredoka+One&display=swap');
  #home{
    text-align: center;
    max-width: 100%;
    /* figure{
        max-width: 100vw;
        min-width:100vw;
        img{
          width: 80%;
          height: auto;
          max-height: 90vh;
          min-height:90vh;
        }
    }*/

    h1{
      font-family: 'Architects Daughter', cursive;
      font-family: 'Fredoka One', cursive;
     
    }

    p{
      font-family: 'Architects Daughter', cursive;
       color:rgb(119, 65, 26);
      //font-size:2vw;
    }
  }
</style>