<template>
  <div class="intro-container">
    <div class="image-section">
      <img class="fade-in" src="https://img2.baidu.com/it/u=2546489114,3802517329&fm=253&fmt=auto&app=138&f=JPEG?w=800&h=1200" alt="个人简介图片" />
    </div>
    <div class="text-section">
      <h1>Mastering the art of cuisine & Designer is my primary focus.</h1>
      <p class="first-line typewriter-effect">
        As a young and passionate chef with a keen eye for design, I seamlessly fuse culinary excellence with aesthetic appeal.
      </p>
      <p class="typewriter-effect">
        My expertise lies in creating dishes that are not only delicious but also visually stunning, ensuring every meal is a feast for both the taste buds and the eyes.
      </p>
      <p class="typewriter-effect">
        With a deep understanding of flavor profiles and a creative approach to presentation, I strive to elevate every dining experience to an art form.
      </p>
      <button @click="showMore">LEARN MORE →</button>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    setTimeout(() => {
      const img = this.$el.querySelector('.fade-in');
      if (img) {
        img.style.transform = 'translateX(0)';
        img.style.opacity = '1';
      }
    }, 500);
  },
  methods: {
    showMore() {
      alert("更多信息...");
    },
  },
};
</script>

<style scoped>
.intro-container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 140vh;
  background: #000;
  color: #fff;
}

.image-section {
  flex: 1;
  padding: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.image-section img {
  max-width: 90%;
  max-height: 100%;
  object-fit: cover;
  transform: translateX(-100%);
  opacity: 0;
  transition: transform 2s ease-in-out, opacity 1s ease-in-out;
}

.text-section {
  flex: 1;
  padding: 20px;
  text-align: left;
}

.text-section h1 {
  font-size: 2.5em;
  margin-bottom: 20px;
}

.text-section p {
  font-size: 1.2em;
  margin-bottom: 20px;
}

.text-section button {
  padding: 30px 100px;
  font-size: 12px;
  border: 1px solid #f7bc4e;
  letter-spacing: 1px;
  background: transparent;
  color: #fff;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  z-index: 1;
}

.text-section button::before {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 0;
  background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23f7bc4e" fill-opacity="1" d="M0,160L48,176C96,192,192,224,288,229.3C384,235,480,213,576,192C672,171,768,149,864,144C960,139,1056,149,1152,165.3C1248,181,1344,203,1392,213.3L1440,224L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
  background-size: cover;
  z-index: -1;
  transition: height 0.5s ease-in-out;
}

.text-section button:hover::before {
  height: 100%;
}

.text-section button:hover {
  color: #fff;
}

.first-line {
  padding-top: 50px;
}
h1 {
  font-family: Georgia, serif;
  padding-right: 100px;
}

p {
  font-family: 'Microsoft YaHei', sans-serif;
  font-size: 1.2em;
  letter-spacing: 0.5px;
  padding-right: 100px;
}
</style>
