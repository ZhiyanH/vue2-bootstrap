<template>
  <div id="app">
      <h2 class="greenFont">My first ever Vue Tutorial</h2>

      <h4 class="blueFont">{{ message }}</h4>

      Name:<input type="text" v-model="name"/> <br> 
      Addr:<input type="text" v-model="addr"/> <br> 
      Email:<input type="text" v-model="email"/> <br> 
      Tel:<input type="text" v-model="tel"/>  <br><br>

      <h2>Name : {{ name }}</h2>
      <h3>Addr :{{ addr }}</h3>
      <h3>Email: {{ email }}</h3>
      <h3>Tel: {{ tel }}</h3>

    <button class="greenFont" @click="increase"> +1</button>
    <button class="redFont" @click="decrease"> -1</button>
    <br>
    <button class="greenFont" @click="increase5"> +5</button>
    <button class="redFont" @click="decrease5"> -5</button>

    <h4 class="blueFont">{{ message }}</h4>

    Name: <input type="text" v-model="name" /> <br>
    Addr: <input type="text" v-model="addr" /> <br>

    Email: <input type="text" v-model="email" /> <br>
    Tel: <input type="text" v-model="tel" /> <br>

    <h2>Name : {{ name }}</h2>
    <h3>Addr : {{ addr }}</h3>
    <h3>Email : {{ email }}</h3>
    <h3>Tel : {{ tel }}</h3>
    
    <button class="blueFont" @click="increase"> +1</button>
    <button class="redFont" @click="decrease"> -1</button>
    <br>
    <button class="blueFont" @click="increase5"> +5</button>
    <button class="redFont" @click="decrease5"> -5</button>
    
    <h2> {{counter}}</h2>
    <br>
    <img v-bind:src="image1">
    <img :src="image2">
    <img :src="image3">
    <br>

</div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      message: "Please enter your details below",
      name: "",
      addr: "",
      email: "",
      tel: "",
      image1: "orange.jpg",
      image2: "strawberry.jpg",
      image3: "apple.jpg",
      url1: "http://apple.com",
      url2: "http://orange.com",
      url3: "http://abc.com",
      web1: "Apple Company",
      web2: "Orange Company",
      web3: "ABC Company",
      counter: 0

    };
  },
  methods: {
    increase() {
      this.counter = this.counter + 1;
    },
    decrease() {
      this.counter = this.counter - 1;
    },
    increase5() {
      this.counter = this.counter + 5;
    },
    decrease5() {
      this.counter = this.counter - 5;
    }
  },
  computed: {},
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}


.blueFont {
  color: blue;
  
}

.greenFont {
  color: green;
  font-size: 30px;
}

.redFont {
  color: red;
  font-size: 30px;
}

.redbg {
  background: red;
}
</style>
