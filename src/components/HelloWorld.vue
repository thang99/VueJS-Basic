<template>
  <div class="hello">
    <h2>Starting</h2>
    <p>Message: {{message}}</p>
    <p>Message Reversed: {{reverseMessage()}}</p>
    <p>Message dùng computed: {{message1}}</p>
    <p>{{now}}</p>
    <hr>
  </div>
</template>

<script>
export default {  
  name: 'HelloWorld',
  data () {
    return {
      message : 'Hello',
      date: new Date()
    }
  },
  methods: {
    reverseMessage() {
        return this.message.split('').reverse().join('');
    }
  },
  computed: {
    message1() {
      return this.message + ' computed';
    },
    now() {
      return this.date;
    }
  },
}
</script>


so sánh computed và methods 
- về cách sử dụng thì computed và methods gần như là giống nhau - ví dụ bên trên
- 1 số lưu ý về computed: 
+ khi gọi computed thì ta không được thêm dấu () đằng sau, nghĩa là computed không nhận tham số đầu vào như methods
+ vì computed không nhận tham số đầu vào, do đó nó chỉ dùng các dữ liệu có sẵn trong data của component
+ điều tuyệt vời của computed là nó được lưu vào bộ nhớ đềm (computed giống useMemo bên Reactjs)
+ computed chỉ tính toán lại khi các biến phụ thuộc trong nó thay đổi, còn methods được tính toán bất kì khi nào 
nó được gọi, nên nếu biết sử dụng computed để tính toán các dữ liệu có sẵn sẽ thì sẽ giúp cải thiện hiệu suất của app
