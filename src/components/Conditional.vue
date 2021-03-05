<template>
  <div id="conditonal">
      <h2>Contional</h2>
      <div id="mark">
          <p v-if="mark >= 8">
            HSG
          </p>
          <p v-else-if="mark >6 && mark <8">
            HSTT
          </p>
          <p v-else>
            HSTB
          </p>
      </div>
      <div id="show">
        <p v-show="mark >= 8">
          HSG
        </p>
        <p v-show="mark>=6 && mark < 8">
          HSTT
        </p>
        <p v-show="mark < 6">
          HSTB
        </p>
      </div>
      <hr>
  </div>
</template>

<script>
export default {
    name:'Conditional',
    data() {
      return {
        mark: 5
      }
    },
}
</script>

So sánh v-if && v-show

+, v-if không render ngay toàn bộ các element mà phụ thuộc vào điều kiện kiểm tra, còn với v-show thì nó sẽ render 
ra tất cả các element từ đầu và chỉ quyết định là có display nó hay không
+, nếu nội dung trong block ít, và trong quá trình sử dụng user tác động đến block nhiều thì dùng v-show sẽ cho tốc độ
tốt hơn, ngược lại dùng v-if
