<template>
  <div id="app">
    <div class="logo">
      <div>
        <img src="./assets/logo.png" alt="Vue.js PWA">
      </div
      ></div>
    <header class="header">
      <div>Vue PWA</div>
    </header>
    <nav class="nav">
      <ul>
        <li>menu 1</li>
        <li>menu 2</li>
        <li>menu 3</li>
      </ul>
    </nav>
    <main class="content">
      <router-view></router-view>
    </main>
    <aside class="sidebar">
      <p>
        Suggestions for improvement welcome, please include screenshots
        and info on your editor or browser version.
      </p>
    </aside>
    <footer class="footer">@Privacy policy</footer>
  </div>
</template>

<script>
export default {
  name: 'app',
};
</script>

<style>
body {
  margin: 0;
}

#app {
  min-height: 100vh;
  margin: 0 auto;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
/*Media query
 0 - 600px Phone
 600px - 900px Tablet portrait
 900px - 1200px Tablet landscape
 1200px - 1800px normal styles
 1800px + Big desktop

*/

@media screen and (max-width: 1800px){
  #app {
    display: grid;
    grid-template-rows: 50px  1fr 50px;
    grid-template-columns: auto 1fr 400px;
    grid-template-areas: "logo header header"
                         "nav content sidebar"
                         "nav footer footer";
  }

  .nav ul {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .header {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

@media screen and (max-width: 960px){
  #app {
    display: grid;
    grid-template-rows: 50px  1fr 50px;
    grid-template-columns: auto 1fr 300px;
    grid-template-areas: "logo header header"
                         "nav content sidebar"
                         "nav footer footer";
  }

  .nav ul {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .header {
    display: flex;
    align-items: center;
  }
}

@media screen and (max-width: 768px){
  #app {
    display: grid;
    grid-template-rows: auto auto 1fr 50px;
    grid-template-columns: auto 1fr;
    grid-template-areas: "logo header"
                         "nav content"
                         "nav sidebar"
                         "footer footer";
  }
  .header {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .nav ul {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

@media screen and (max-width: 560px){
  #app {
    display: grid;
    grid-template-rows: 50px 50px auto 1fr auto auto;
    grid-template-columns: 1fr;
    grid-template-areas: "logo"
                         "header"
                         "nav"
                         "content"
                         "sidebar"
                         "footer";
  }
  .header {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .nav ul {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
  }
  .nav {
    padding: 0;
  }
}

main {
  text-align: center;
}

header {
  margin: 0;
  padding: 0 16px 0 24px;
  background-color: #35495E;
  color: #ffffff;
}

 .logo div img{
  width: 60px;
  height: 60px;
}

 .logo div {
   display: flex;
   flex-direction: row;
   align-items: center;
   justify-content: center;
 }

 .logo {
   grid-area: logo;
 }
.header {
  grid-area: header;
  font-size: 18px;
  font-weight: bold;
  color: #fff;
}
.nav {
  grid-area: nav;
  background-color: #35495E;
  color: #fff;
  font-size: 16px;
  font-weight: bold;

}

.content {
  grid-area: content;
  padding: 10px;
  background-color: #5f9ea036;
  color: #000;
}
.sidebar {
  grid-area: sidebar;
  padding: 10px;
  background-color: #add8e68a;
  color: black;
}
.footer {
  grid-area: footer;
  background-color: #35495E;
  color: #fff;
  padding: 10px;
  text-align: center;
}


</style>
