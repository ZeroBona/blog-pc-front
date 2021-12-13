<template>
  <div class="home">
    <div class="blog-list">
      <div v-for="item in blogList" :key="item.id" class="blog-item">
        <h3 class="omit-word-1">{{item.title}}</h3>
        <p class="omit-word-1">{{item.surmary}}</p>
        <div class="blog-info">
          <span>{{item.createTime}}</span>
          <div class="blog-nums">
            <span>{{item.readNum}}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
  components: {},
  data(){
    return {
      blogList: [
        {
          id: '12312',
          title: '这是一个标题',
          surmary: '这是一个简介文字',
          createTime: '2021-11-28 23:12:32',
          readNum: 12,
        },
        {
          id: '1231212',
          title: '这是一个标题',
          surmary: '这是一个简介文字',
          createTime: '2021-11-28 23:12:32',
          readNum: 12,
        },
      ],
    };
  },
}
</script>
<style lang="less" scoped>
.common-box {
  padding: 0 20px;
  border-radius: 6px;
  background-color: #fff;
  box-shadow: 0 6px 10px 0 rgb(20 36 70 / 8%);
}
.blog-list{
  .common-box();
}
.blog-item{
  border-bottom: 1px solid #dcdfe6;
  padding: 10px 0;
  cursor: pointer;
  &:hover{
    color: #347fff;
  }
  &:last-of-type{
    border-bottom: none;
  }
  >h3{
    line-height: 30px;
    font-size: 16px;
  }
  >p{
    margin-bottom: 4px;
    line-height: 30px;
    font-size: 14px;
  }
  .blog-info{
    display: flex;
    justify-content: space-between;
  }
}
</style>
