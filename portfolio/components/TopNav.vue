<template>
  <nav class="top-nav">
    <ul>
      <li v-for="item in items" :key="item.id">
        <a :href="item.url">
          <i class="im" :class="item.icon" aria-hidden="true" />

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
        { id: 0, name: 'Intro', url: '#intro', icon: 'im-home' },
        { id: 1, name: 'Yejun', url: '#my-profile', icon: 'im-star' },
        { id: 2, name: 'Value', url: '#my-value', icon: 'im-rocket' },
        { id: 3, name: 'Works', url: '#my-works', icon: 'im-windows-o' },
        { id: 4, name: 'Skills', url: '#my-skills', icon: 'im-layer' }
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

  .top-nav ul li .im {
    font-size: 15px;
    margin-right: 1.5px;
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
    .top-nav ul li .im {
      display: none;
    }

    .top-nav ul li span {
      font-size: 12px;

      display: inline;
    }
  }

  @media screen and (min-width: 1000px) {
    .top-nav ul li .im {
      font-size: 13px;
      margin-right: 5px;

      display: inline;
    }

    .top-nav ul li span {
      font-size: 15px;
    }
  }
</style>
