<template>
  <div class="blogs">
    <ul>
      <li v-for="item in blogs" :key="item.id">
        <div class="blog">
          <div class="blog-title">
            <a href="javascript:void(0)" @click="titleClick">{{item.title}}</a>
          </div>
          <div class="blog-summary">{{item.summary}}</div>
          <div class="blog-common">
            <div class="publish-date">{{item.date}}</div>
            <div class="interactive">
              <a href>点赞:{{item.interactive}}</a>
              <a href>阅读:{{item.read}}</a>
              <a href>评论:{{item.comment}}</a>
            </div>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Blogs",
  props: {
    blogs: {
      type: Array,
      default: []
    }
  },
  data() {
    return {};
  },
  components: {},
  created() {},
  mounted() {},
  methods: {
    titleClick() {
      this.$router.push("/about");
    }
  }
};
</script>

<style scoped>
.blog {
  height: 100px;
  text-align: left;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.blog-title {
  font-size: 21px;
  font-weight: 600;
  line-height: 24px;
}
.blog-title a {
  color: black;
}
.blog-title a:hover {
  color: red;
}
.blog-summary {
  display: inline;
  color: #8a8a8a;
  font-size: 14px;
  line-height: 36px;
}

.publish-date,
.interactive {
  display: inline-block;
}

.publish-date {
  font-size: 15px;
}

.interactive {
  float: right;
}
.interactive a {
  margin: 0 10px;
}
</style>
