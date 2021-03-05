<template>
  <form action="" method="post">
      <h2>Input</h2>
      <input type="text" v-model.lazy.trim="message"> &nbsp;
      <span>message: {{message}}</span>
      <br>
      <br>  
      <input type="radio" id="" v-model="gender" value="Nam">Nam 
      <input type="radio" id=""  v-model="gender" value="Nữ">Nữ &nbsp;
      <span>gender: {{gender}}</span>
      <br>
      <br>
      <input type="checkbox" value="taxi" v-model="selected">Taxi
      <input type="checkbox" value="bus" v-model="selected">Bus
      <input type="checkbox" value="bike" v-model="selected">Bike &nbsp;
      <span>phuong tien: {{selected}}</span>
      <br>
      <br>
      <select v-model="select">
          <option disabled value="">Correct answer</option>
          <option>A</option>
          <option>B</option>
          <option>C</option>
      </select> &nbsp;
      <span>you choose:{{select}}</span>
      <br>
      <br>
      <input type="number" v-model.number="number">
      <span>number: {{number}}</span>
  </form>
</template>

<script>
export default {
    data() {
        return {
            message: '',
            gender:'',
            selected: [],
            select:'',
            number:''
        }
    },
}
</script>

<style>

</style>