<!--  EnvironmentalDisplay.vue  -->
  
<template>
  <div class="instagram-feed">
    <h3 class="feed-title">MY INSTAGRAM FEED</h3>
    <h1 class="main-title">Me as a Lively Girl.</h1>
    <div class="image-gallery">
      <div class="image-wrapper" v-for="(image, index) in images" :key="index">
        <img :src="image" alt="Instagram Image" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        "https://img1.baidu.com/it/u=1807070079,4252475929&fm=253&fmt=auto&app=120&f=JPEG?w=800&h=1422",
        "https://img2.baidu.com/it/u=54421408,4206793300&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=1083",
        "https://qcloud.dpfile.com/pc/GYyKIR78Zc8QAET-BI1rzQrN3ASQWrrWft4MtVTONBqhow6pX0gWG-2v4NsvChrI.jpg",
        "https://img2.baidu.com/it/u=1966266789,2683995189&fm=253&fmt=auto&app=138&f=JPEG?w=800&h=1576",
        "https://img1.baidu.com/it/u=1207584750,3772597574&fm=253&fmt=auto&app=120&f=JPEG?w=800&h=1200",
      ],
    };
  },
};
</script>

<style scoped>
.instagram-feed {
  background-color: black;
  color: white;
  text-align: center;
  padding: 100px 0;
  font-family: 'Georgia', serif;
}

.feed-title {
  font-size: 0.8em;
  color: #d49a6a;
  letter-spacing: 2px;
  margin-bottom: 20px;
}

.main-title {
  font-size: 54px;
  margin-bottom: 120px;
  margin-top: 0px;
  letter-spacing: 1px;
}

.image-gallery {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.image-wrapper {
  margin: 0 10px;
  width: 250px;
  height: 500px;
  overflow: hidden;
}

.image-wrapper img {
  width: 100%;
  height: auto;
}
</style>
