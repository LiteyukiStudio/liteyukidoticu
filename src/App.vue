<template>
  <h1 style="text-align: center">Liteyuki Studio Index 索引页</h1>
  <h3>轻雪相关内容</h3>
  <a href="https://mc.liteyuki.icu" class="button">Liteyuki Server 服务器官网</a>
  <a href="https://meme.liteyuki.icu" class="button">Liteyuki Memes</a>
  <a href="https://lab.liteyuki.icu" class="button">Liteyuki 社区</a>
  <a href="https://bot.liteyuki.icu" class="button">Liteyuki Bot</a>
  <a href="https://nd.liteyuki.icu" class="button">Liteyuki Netdisk</a>
  <h3>其他内容</h3>
  <a href="https://sfkm.me" class="button">SnowyKami 个人主页</a>
  <a href="https://tcea.top" class="button">白鼠的小站</a>
  <a href="https://minecraft.net" class="button">Minecraft 官网</a>
  <footer>
    <hr>
    <a href="https://icp.gov.moe/?keyword=20240224" target="_blank">萌ICP备20240224号</a>
    <p>© 2020-2024 Liteyuki Studio</p>
  </footer>
</template>

<script>
export default {
  name: 'App',
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  font-family: 'Arial', sans-serif;
  margin: 10px;
  padding: 5px;
  background-color: #f5f5f5;
  text-align: center;
  align-content: center;
  overflow-x: hidden; /* 隐藏水平溢出 */
}

h1 {
  color: #333;
}

h3 {
  color: #555;
}

a.button {
  align-content: center;
  display: block;
  margin: 10px auto; /* 居中 */
  padding: 15px 15px; /* 调整上下间距 */
  color: #fff;
  text-decoration: none;
  background-color: #a2d8f4;
  border-radius: 80px;
  transition: background-color 0.3s ease;
  max-width: 80%;
}

a.button:hover {
  background-color: #d0e9ff;
}

@media (max-width: 1080px) {
  /* 在小屏幕上，每行显示一个按钮 */
  a.button {
    width: calc(100% - 20px);
  }
}
</style>
