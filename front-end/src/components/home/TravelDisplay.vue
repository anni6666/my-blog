<!--
 * @Date: 2025-02-14 11:50:49
 * @LastEditors: Aregene
 * @LastEditTime: 2025-02-14 13:18:27
-->

<!--  TravelDisplay.vue  -->

<template>
  <div class="blog-showcase">
    <h2 class="title">Latest Blog Posts</h2>
    <h3 class="description">
      Read through my thoughts and insights through being a Great Cook.
    </h3>
    <div class="blog-images">
      <div class="image-card" v-for="(blog, index) in blogs" :key="index">
        <img :src="blog.image" alt="Blog Image" />
        <div class="image-text">
          <h4>{{ blog.title }}</h4>
          <p>{{ blog.description }}</p>
          <a href="#" class="image-caption">Read More</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      blogs: [
        {
          image:
            "https://img0.baidu.com/it/u=2648199945,244004265&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=625",
          title: "I started a vlog",
          description:
            "Building SquaR is a weekly vlog series documenting my journey...",
        },
        {
          image:
            "https://img2.baidu.com/it/u=1643992979,2273380359&fm=253&fmt=auto&app=133&f=JPEG?w=380&h=675",
          title: "Introducing SQUAR",
          description:
            "Today I’d like to introduce everyone to my new company, SQUAR...",
        },
        {
          image:
            "https://img1.baidu.com/it/u=164334912,3393174090&fm=253&fmt=auto&app=120&f=JPEG?w=500&h=1083",
          title: "Code Shop growth",
          description:
            "My Code Shop was started as an idea to support the community...",
        },
      ],
    };
  },
};
</script>

<style scoped>
.blog-showcase {
  background-color: black;
  color: white;
  text-align: center;
  padding: 40px 0;
  font-family: "Georgia", serif;
}

.title {
  font-size: 14px;
  font-weight: bold;
  color: #d49a6a; /* 标题的颜色 */
  text-align: left; /* 标题左对齐 */
  padding-left: 300px;
  margin-bottom: 10px; /* 取消下边距 */
  padding-right: 50px;
}

.description {
  font-size: 44px;
  color: white; /* 描述的颜色 */
  text-align: left; /* 描述左对齐 */
  padding-left: 300px;
  padding-right: 350px;
  margin-top: 15px; /* 取消上边距，如果需要的话 */
  padding-bottom: 100px;
}

.blog-images {
  display: flex;
  justify-content: center;
}

.image-card {
  margin: 0 10px;
  text-align: left;
  flex: 1;
}

.image-card img {
  width: 100%;
  height: auto;
}

.image-text {
  padding: 10px;
}

.image-text h4 {
  margin: 10px 0;
}

.image-text a {
  color: #f7bc4e;
  text-decoration: none;
}

.image-caption {
  font-size: 14px;
  margin-top: 5px;
  position: relative;
  display: inline-block;
  color: #d5aa80; /* 文字颜色 */
  text-transform: uppercase; /* 大写字母 */
  letter-spacing: 2px; /* 字母间距 */
  text-align: left; /* 向左靠齐 */
}

.image-caption::after {
  content: "";
  display: block;
  width: 100%;
  height: 2px;
  background-color: #d5aa80; /* 下划线颜色 */
  position: absolute;
  bottom: -5px; /* 距离文字底部的距离 */
  left: 0;
}
</style>
