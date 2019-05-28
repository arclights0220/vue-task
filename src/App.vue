<template>
  <div id="app">
    <div class="list">  
      <ul>
      <li v-for="(text, idx) in texts" :key="idx">
        {{text}} 
        <button @click="texts.splice(idx,  1)">boom!</button>
        </li>
      </ul>
    </div><br>
    <div>
     <input type="text" v-model="newTexts" class="text"/>
     <button @click="texts.push(newTexts)">push</button>
     </div>
  </div>
</template>

<script>
//eslint-disable-next-line
import txt from "./components/txt";
export default {
  name: "App",
  data() {
    return {
      texts: ['push', 'and', 'delete', 'anything'],
      newTexts: ''
    };
  },

  components: {
    asdf:txt
  }
};
</script>

<style>
body{
  width: 100vw;
  height: 100vh;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  flex-wrap: wrap;
}
  li{
    list-style: none;
    margin: 10px;
  }
  #app{
    width: 50vw;
    height: 50vh;
    border: 1px none black;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    font-size: 1.5em;
    background-color: #3f4;
    margin-left: 0;
  }
  .text{
    font-size: 1.1em;
  }
  button{
    font-size: 1.1em;
  }
</style>
