<template>
  <div id="app">
    <header>
      <div>
        <h1>Renam Freitas</h1>
        <h2>FRONT-END DEVELOPER</h2>
      </div>
      <h3>{{ $route.name }}</h3>
    </header>

    <transition name="fade" mode="out-in">
      <router-view/>
    </transition>
    
    <ul class="main-menu">
      <li><router-link v-bind:to="'/'">Home</router-link></li>
      <li><router-link v-bind:to="'/about'">About</router-link></li>
      <li><router-link v-bind:to="'/contact'">Contact</router-link></li>
    </ul>

    <ul class="social">
      <li><a target="_blank" href='https://www.facebook.com/renamdefreitas'>Facebook</a></li>
      <li><a target="_blank" href='https://www.instagram.com/renamfreitas/'>Instagram</a></li>
      <li><a target="_blank" href='https://www.linkedin.com/in/renam-freitas-02467572/'>Linkedin</a></li>
      <li><a target="_blank" href='https://github.com/renamfreitas'>GitHub</a></li>
    </ul>

  </div>
</template>
<script>
export default {
  name: 'App'
}
</script>
<style lang="scss">
html {
    height: 100%;
}
body {
  background-image: url('./assets/bground.jpg');
  background-size: cover;
  background-color: #000;
  margin: 0;
}
</style>
<style lang="scss" scoped>

@font-face {
  font-family: 'BigNoodleTitling-Oblique';
  src: url('./assets/fonts/BigNoodleTitling-Oblique.eot?#iefix') format('embedded-opentype'),
       url('./assets/fonts/BigNoodleTitling-Oblique.woff')       format('woff'),
       url('./assets/fonts/BigNoodleTitling-Oblique.ttf')        format('truetype'), url('./assets/fonts/BigNoodleTitling-Oblique.svg#BigNoodleTitling-Oblique') format('svg');
  font-weight: normal;
  font-style: normal;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;

  header {
    display: flex;
    justify-content: space-between;
    padding: 80px 80px 0;

    > div {
      text-align: left;

      h1 {
        font-family: 'BigNoodleTitling-Oblique';
        font-size: 90px;
        color: #17ffff;
        font-weight: normal;
        transform: skew(-10deg, 0);
        width: 420px;
        margin: 0;
      }

      h2 {
        font-family: 'BigNoodleTitling-Oblique';
        font-size: 50px;
        color: #fff;
        font-weight: normal;
        transform: skew(-10deg, 0);
        margin: 0;
      }
    }

    h3 {
      font-family: 'BigNoodleTitling-Oblique';
      font-size: 90px;
      color: #fff;
      font-weight: normal;
      transform: skew(-10deg, 0);
      margin: 0;
    }
  }
  
  img {
    height: 80px;
  }

  ul.main-menu {
    position: fixed;
    bottom: 0;
    list-style: none;
    display: flex;
    justify-content: center;
    width: 100%;
    margin: 0 0 60px;

    li {
      margin: 0 20px;
      a {
        color: #17ffff;
        text-decoration: none;
        font-weight: 700;
        font-size: 42px;
        font-family: 'BigNoodleTitling-Oblique';
        font-weight: normal;
        transform: skew(-10deg, 0);
      }
    }
  }

  ul.social {
    list-style: none;
    display: flex;
    justify-content: center;
    padding: 0;
    margin: 40px 0 30px;

    li {
      margin: 0 5px;
      a {
        display: block;
        background: black;
        border-radius: 5px;
        height: 30px;
        line-height: 30px;
        color: white;
        text-decoration: none;
        text-transform: uppercase;
        font-weight: 700;
        font-size: 10px;
        padding: 0 10px;
      }
    }
  }
}

.fade-enter-active, .fade-leave-active {
  transition: all .5s ease;
}
.fade-enter, .fade-leave-active {
  opacity: 0
}
.child-view {
  position: absolute;
  transition: all .5s cubic-bezier(.55,0,.1,1);
}
.slide-left-enter, .slide-right-leave-active {
  opacity: 0;
  -webkit-transform: translate(30px, 0);
  transform: translate(30px, 0);
}
.slide-left-leave-active, .slide-right-enter {
  opacity: 0;
  -webkit-transform: translate(-30px, 0);
  transform: translate(-30px, 0);
}
</style>
