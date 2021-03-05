<template>
  <div id="for">
      <h2>For</h2>
      <p>With Array:</p>
      <li v-for="sport in sports" :key="sport.id">
          {{ sport.id }}- {{ sport.name }}- {{ sport.team }}
      </li>
      <p>With Object:</p>
    <li v-for="(value, key) in person" :key="key">
        {{key}}:{{value}}
    </li>
    <span>Các số chẵn có trong mảng là:</span> 
    <span v-for="n in evenNumber" :key="n.id">
      {{ n }}
    </span>
    <br>
    <span>Các số lớn hơn 3 là:</span>
    <span v-for="item in numbers" :key="item.id" >
        <span v-if="item>3">
             {{ item }}
        </span>
    </span>
    <hr>
  </div>
</template>

<script>
export default {
    data() {
        return {
            sports: [
                {id:1, name:'football', team:2},
                {id:2, name:'tennis', team:2}
            ],
            person: {
                name:'Peter' ,
                age:18
            },
            numbers:[1,2,3,4,5,6]
        }
    },
    computed: {
        evenNumber() {
            return this.numbers.filter((number) => number%2===0 ); 
        }
    },
}
</script>
