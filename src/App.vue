<template>
  <div id="app">
    <img src="./assets/logo.svg">
    <ul class="main-menu">
      <li><router-link v-bind:to="'/'">Home</router-link></li>
      <li><router-link v-bind:to="'/about'">About</router-link></li>
      <li><router-link v-bind:to="'/contact'">Contact</router-link></li>
    </ul>

    <transition name="fade" mode="out-in">
      <router-view/>
    </transition>
    
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

<style lang="scss" scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
  img {
    height: 80px;
  }

  ul.main-menu {
    list-style: none;
    display: flex;
    justify-content: center;

    li {
      margin: 0 10px;
      a {
        color: #2c3e50;
        text-decoration: none;
        font-weight: 700;
        font-size: 22px;
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

</style>

<style>
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
