<template>
  <nav class="top-nav">
    <ul>
      <li v-for="item in items" :key="item.id">
        <a :href="item.url">
          <img class="icon" :src="item.src">

          <span>{{ item.name }}</span>
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'TopNav',
  data () {
    return {
      items: [
        { id: 0, name: 'Intro', url: '#intro', src: 'icons/home.png' },
        { id: 1, name: 'Yejun', url: '#my-profile', src: 'icons/star.png' },
        { id: 2, name: 'Value', url: '#my-value', src: 'icons/rocket.png' },
        { id: 3, name: 'Works', url: '#my-works', src: 'icons/window.png' },
        { id: 4, name: 'Skills', url: '#my-skills', src: 'icons/layer.png' }
      ]
    }
  }
}
</script>

<style>
  .top-nav {
    display: flex;
  }

  .top-nav ul li {
    float: left;
    list-style: none;
    padding: 3px 10px;
    margin: 0 5px;
  }

  .top-nav ul li::after {
    color: #ba451a;
    content: '/';
    font-size: 10px;
    padding-left: 20px;
  }

  .top-nav ul li:last-child::after {
    content: '';
    padding-left: 10px;
  }

  .top-nav ul li a {
    vertical-align: middle;
  }

  .top-nav ul li .icon {
    width: 15px;
    margin-right: 1.5px;
    filter: grayscale(1) brightness(0) invert(1);
    transform: translateY(1px);
  }

  .top-nav ul li a {
    color: white;
    text-decoration: blink;
  }

  .top-nav ul li span {
    font-size: 10px;
    text-transform: uppercase;

    display: none;
  }

  @media screen and (min-width: 600px) {
    .top-nav ul li .icon {
      display: none;
    }

    .top-nav ul li span {
      font-size: 12px;

      display: inline;
    }
  }

  @media screen and (min-width: 1000px) {
    .top-nav ul li .icon {
      width: 13px;
      margin-right: 5px;

      display: inline;
    }

    .top-nav ul li span {
      font-size: 15px;
    }
  }
</style>
