<template>
  <div class="hello">
    <h1>
      这里是scss测试
    </h1>
    <div class="storetest">{{storetest}}</div>
    <el-button>这是个无效的点击按钮</el-button>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'HelloWorld',
  data () {
    return {
      storetest: ''
    }
  },
  mounted () {
    this.storetest = this.$store.state.count;
    axios.get(onlinedomain+'/media/latest?category_id=10373&sort=1&size=3&page=1&channel_id=247&weight=2')
      .then(response=>{
        console.log(response)
      })
      .catch(error => {
          console.log(error);
      });

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h1{
  font-weight: 100;
  color: $red;
  background: $blue;
}
</style>
