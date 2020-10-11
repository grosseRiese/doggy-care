<template>
  <section id="doginfo">
    <figure>
      <img :src="dog.img" :alt="dog.name" />
    </figure>
    <h1>{{dog.name}}</h1>
    <aside class="info">
        <section>
            <p><b>Breed: </b>{{dog.breed}}</p>        
            <p><b>Age: </b>{{dog.age}}y</p>        
            <p><b>Chip Number: </b>{{dog.chipNumber}}</p>
        </section>
        <section>
            <p><b>Owner:</b> {{ dog.owner.name }} {{ dog.owner.lastName }}</p>
            <p>Phone: {{dog.owner.phoneNumber}}</p>
        </section>

    </aside>

  </section>
</template>

<script>
export default {
 name: 'DogInfo',
 props: {
     dogs: Array
 },
 computed: {
    dog(){ 
        return this.dogs.filter(dog => dog.chipNumber === this.$route.params.chipNumber)[0]
    }
 }
}
</script>
<style lang="scss">

#doginfo{
    box-shadow:5px 8px 16px 5px rgba(0,0,0,0.2);
    width:40%;
    margin-left: 35%;
    margin-right: 35%; 
    text-align: center;
    font-size:2vw;

    img {
        max-width: 100%;
        
      }

      p{
        color:rgb(187, 187, 187);
          
      }

      &:hover {
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
      }
  }
</style>
<!-- <style lang="scss">
    #doginfo {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-auto-rows: 6rem;

        figure {
            margin: 0;
            padding: 0;
            grid-column: auto / span 1;
            grid-row: auto / span 3;
            display: flex;
            justify-content: center;
            align-items: center;

            img {
                width: 12rem;
                height: 12rem;
                object-fit: cover;
                border-radius: 999rem;
            }

        }

        h1 {        
            grid-column: auto / span 2;
            font-size: 3rem;
            margin: 0;
            padding: 0;
            display: flex;
            align-items: flex-end;
        }

        .info {
            display: flex;
            grid-column: auto / span 2;

            > section {
                width: 100%;
                

                h2 {
                    margin: 0;
                    padding: 0;
                    font-weight: 400;
                }
            }
        }
    }
</style>-->