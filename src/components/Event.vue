<template>
  <div id="event">
      <button v-on:click="increament()">Click</button>
      <span>You clicked {{count}} times</span>
      <hr>
  </div>
</template>

<script>
export default {
    name:'Event',
    data() {
        return {
            count: 0
        }
    },
    methods: {
        increament() {
            this.count++;
        }
    },
}
</script>

v-on:sbumit.prevent : không reload lại trang
v-on:click.once : sự kiện nhấp chuột được kích hoạt nhiều nhất là 1 lần
v-on:keyup.enter : chỉ gọi sự kiện khi nhấn enter
v-on:scroll.passive="onScroll" : hành vi mặc định của sự kiện scroll sẽ xảy ra ngay lập tức, thay vì đợi 'onScroll' hoàn tất
