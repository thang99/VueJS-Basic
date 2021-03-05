<template>
  <div id="class">
      <h2>Style && Class</h2>
      <p v-bind:class="{active: isActive, hide: isHide}">This is my classroom</p>
      <button v-on:click="changeColor()">Click</button>
      <button v-on:click="changeStatus()">Click 1</button>
      <p v-bind:style="{'color':'blue'}">Hi everyone !</p>
      <!-- <p style='color:blue'>Hi everyone !</p> -->
      <p v-bind:style="{'color':color}">Hello world</p>
      <hr>
  </div>
</template>

<script>
export default {
    name:'Class',
    data() {
        return {
            isActive: false,
            isHide: false,
            color: 'orange'
        }
    },
    methods: {
        changeColor() {
            this.isActive = true;
        },
        changeStatus() {
            this.isHide = true;
        }
    },
}
</script>
<style scoped>
.active {
    color:red;
}
.hide {
    display: none;
}
</style>