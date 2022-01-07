<template>
  <div class="home-container">
    <ul>
      <li v-for="item in list">{{ item.content }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data: () => ({
    list: [],
  }),
  mounted() {
    this.$http
      .get("http://localhost:3000/comment/music?id=186016&limit=1")
      .then((res) => {
        console.log(res.data.hotComments);
        this.list = res.data.hotComments;
      });
    console.log(1);
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<style>
.home-container ul li {
  line-height: 20px;
}
</style>
