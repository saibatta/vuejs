<template>
  <div class="ist-rendring-container">
    <h3>{{ msg }}</h3>
    <div class="divider"></div>
    <h3>v-for directive to iterate items in array </h3>
    <li v-for="(item, index) in listOne" :key="item">
      {{ index }} -- {{ item }}
    </li>

    <div class="divider"></div>
    <h3>v-for diretive to iterate object Key/values</h3>
    <li v-for="( key, value ) of listTwo" :key="key">
      {{ key }} -- {{ value }}
    </li>

    <div class="divider"></div>
    <h3>v-for directive destructive values from array list</h3>
    <li v-for="({ message }, index ) in thirdOne" :key="message">
      {{ index }} -- {{ message }}
    </li>


    <div class="divider"></div>
    <h3>nested v-for directive array list</h3>
    <div v-for="(item, index ) in fourthOne" :key="item">
      Outer : {{ index }} -- {{ fourthOne[index] }}
      <div v-for="(key, value, InnerIndex) of item" :key="InnerIndex">
        Inner : {{ InnerIndex }} -- {{ key }} --{{ value }}
        <div v-for="(innerKey, innerValue, innerInIndex) of key" :key="innerInIndex">
          Deep Inner : {{ innerKey }} -- {{ innerValue }}
        </div>
      </div>
    </div>

    <div class="divider"></div>
    <h3> v-for directive template array</h3>
    <ul>
      <template v-for="item in listOne" :key="item">
        <li>
          {{ item }}
        </li>
      </template>
    </ul>


  </div>
</template>

<script>
export default {
  name: 'ListRendering',
  props: {
    msg: String
  },
  data() {
    return {
      listOne: ['hello', 'hi', 'vueJS', 'React', 'Angular'],
      listTwo: {
        firstKey: 'First Value',
        secondKey: "Second Value",
        thirdKey: 'Third Value'
      },
      thirdOne: [
        { message: 'JS' },
        { message: 'HTML' },
        { message: 'CSS' }
      ],
      fourthOne: [
        { itemOne: [{ itemOne1: 'Item One 1' }, { itemOne2: 'Item One 2' }] },
        { itemTwo: [{ itemTwo1: 'Item Two 1' }, { itemTwo2: 'Item Two 2' }] },
        { itemThree: [{ itemThreee1: 'Item Three 1' }, { itemThreee2: 'Item Three 2' }] }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.list-rendring-container {
  height: 90vh;
  background-color: aliceblue;

}

.divider {
  border: 1px dashed black;
  width: 70%;
  margin: auto;
}
</style>
