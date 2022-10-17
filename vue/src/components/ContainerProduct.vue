<template>
  <div class="product">
      <div class="Bigcontainer">
          <div class="title">
            <ul id="titles">
              <li>
                <h1>{{ name}}</h1>
              </li>
              <li>
                <p2>{{extendedName}}</p2>
              </li>
            </ul>
          </div>
        <div class="container">
  <!--         <img src={{image}}/> -->
          <img src="https://media.ldlc.com/r374/ld/products/00/05/90/02/LD0005900230_1.jpg" />
          <p class="description">{{description}}</p>
          <div class="price">
            <p1>{{price}}</p1>
          </div>
        </div>
        
      </div>
      
  </div>

  <div class="dataSheet">
    <h1> Fiche Technique</h1>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ContainerProduct',
  props: {
    name: String,
    extendedName : String,
    description : String,
    image : String,
    price : String
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.product{
  display: flex;
  justify-content: center;
  margin : 20px;
  align-items: center;
  background: rgba(52, 75, 157, 0.1);
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 50px;
}
.title{
  display:flex;
  font-size: small;
}
li{
  list-style-type:none;
}

.Bigcontainer{
  margin : 50px
}

.container{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-left: 50px;
  margin-right: 50px;
  margin-top: 50px;
}

.description{
 display :flex;
 justify-content: center;
 align-items: center;
 white-space:unset;
 color:blue;
 font-size: small;
 width:20%;
}

.price{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 250px;
  height: 150px;
  background: rgba(52, 75, 157, 0.6);
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 50px;
  color:aliceblue;
  font-weight: bold;
  font-size: x-large;
}

.dataSheet{
  display: flex;
  border: red solid;

}

</style>
