<template>
  <div class="squarespace-container">
    <h1>My Recipe Collection</h1>
    <div class="card-container">
      <div class="card" v-for="(item, index) in cards" :key="index">
        <h2>{{ item.title }}</h2>
        <p>{{ item.description }}</p>
        <div class="button-container">
          <a class="button" href="#">{{ item.linkText }}</a>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      cards: [
        {
          title: '鲁菜 Shandong Cuisine',
          description: 'Shandong Cuisine, from Shandong province, is famous for its seafood dishes, strong flavors, and traditional cooking methods.',
          linkText: 'LEARN MORE',
        },
        {
          title: '川菜 Sichuan Cuisine',
          description: 'Sichuan Cuisine, known for its spicy kick, blends Sichuan pepper and chili peppers for a tangy, savory experience. A must-try in Chinese gastronomy.',
          linkText: 'LEARN MORE',
        },
        {
          title: '粤菜 Cantonese Cuisine',
          description: 'Cantonese Cuisine, hailing from Guangdong, China, is renowned for its fresh ingredients, delicate flavors, and diverse cooking methods.',
          linkText: 'LEARN MORE',
        },
        {
          title: '淮扬菜 Huaiyang Cuisine',
          description: 'Huaiyang Cuisine, originating from Jiangsu, China, is famous for its refined techniques, fresh ingredients, and subtle, elegant flavors.',
          linkText: 'LEARN MORE',
        },
        {
          title: '闽菜 Fujian Cuisine',
          description: 'Fujian Cuisine, from Fujian province, features fresh seafood, unique flavors, and a blend of sweet, sour, and savory tastes.',
          linkText: 'LEARN MORE',
        },
        {
          title: '浙菜 Zhejiang Cuisine',
          description: 'Zhejiang Cuisine, hailing from Zhejiang province, is known for its fresh ingredients, delicate flavors, and emphasis on seafood dishes.',
          linkText: 'LEARN MORE',
        },
        {
          title: '湘菜 Hunan Cuisine',
          description: 'Hunan Cuisine, originating from Hunan province, is renowned for its spicy, sour, and savory flavors, utilizing fresh ingredients and bold seasoning.',
          linkText: 'LEARN MORE',
        },
        {
          title: '徽菜 Anhui Cuisine',
          description: 'Anhui Cuisine, hailing from Anhui province, is characterized by its rich flavors, use of wild herbs, and emphasis on cooking techniques.',
          linkText: 'LEARN MORE',
        },
      ],
    };
  },
};
</script>

<style scoped>
.squarespace-container {
  background-color: #000;
  color: #fff;
  text-align: center;
  padding: 10px 0;
  padding-bottom: 100px;
}

h1 {
  font-size: 4em;
  margin-bottom: 50px;
  font-weight: bold;
  padding-bottom: 30px;
}

.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.card {
  background-color: #111;
  padding: 20px;
  width: 300px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
}

.button-container {
  position: relative;
  margin-top: 10px;
}

.button {
  position: relative;
  display: inline-block;
  padding: 10px 20px;
  color: #f7bc4e;
  text-decoration: none;
  font-weight: bold;
  border: 2px solid #f7bc4e;
  overflow: hidden;
  z-index: 1; /* 确保文字始终在色块之上 */
}

.button::after {
  content: '';
  position: absolute;
  bottom: 100%;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #f7bc4e;
  transition: bottom 0.3s;
  z-index: -1; /* 确保色块始终在文字之下 */
}

.button:hover::after {
  bottom: 0;
}

.button:hover {
  color: #111; /* hover时改变文字颜色 */
  z-index: 1;
}

.card h2 {
  font-size: 1.5em;
  margin-bottom: 15px;
}

.card p {
  font-size: 1em;
  line-height: 1.5;
  margin-bottom: 20px;
}
</style>
