<template>
  <div class="about">
    <h1>{{ msg }}</h1>
    <p>HI, I’M RENAM.</p>
    <h3>I design &amp; build web aplications, user interfaces, landing pages and some other things, with over 10 years of web development experience.</h3>
    <h3>Academic background</h3>
    <p>
    2007/2008 – Panamericana School of Art and Design – Graphic Design<br />
    2007/2010 – Uniso University – Bachelor Degree in Graphic Design
    </p>
    <h3>Code</h3>
    <p>I design in the browser with HTML(5), CSS(3) and a touch of JavaScript. I can code things from scratch, but I like to&nbsp;work with front-end frameworks.</p>
    <h3>Design</h3>
    <p>Some of the softwares that I love to use are Photoshop, Illustrator, Premiere, Swift3d and Animate.</p>
    <p>I’am a citizen of Brazil and Portugal.</p>
  </div>
</template>

<script>
export default {
  name: 'About',
  data () {
    return {
      msg: 'About ME'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
