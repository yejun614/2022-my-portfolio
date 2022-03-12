<template>
  <nav class="top-nav">
    <ul>
      <li v-for="item in items" :key="item.id">
        <a :href="item.url">
          {{ item.name }}
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
        { id: 0, name: 'Intro', url: '#intro' },
        { id: 1, name: 'Yejun', url: '#my-profile' },
        { id: 2, name: 'Value', url: '#my-value' },
        { id: 3, name: 'Works', url: '#my-works' },
        { id: 4, name: 'Skills', url: '#my-skills' }
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
    color: white;
    font-size: 15px;
    text-decoration: blink;
    text-transform: uppercase;
  }
</style>
