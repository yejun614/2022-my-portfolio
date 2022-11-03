<template>
  <section id="my-works">
    <h1>작업물</h1>

    <div class="cover">
      <a
        v-for="item in items"
        :key="item.id"
        class="box"
        :style="{'background-color': item.color}"
        :href="item.href"
        target="_blank"
      >
        {{ item.name }}
      </a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyWorks',
  data () {
    return {
      items: [
        { id: 0, name: 'Tetris Game', color: '#05C7F2', href: 'https://yejun614.github.io/html5-games/games/tetris/' },
        { id: 1, name: 'Calendar', color: '#03588C', href: 'https://codepen.io/yejun614/pen/yLgwEJG' },
        { id: 2, name: 'Color Picker', color: '#012E40', href: 'https://codepen.io/yejun614/pen/bGgvvwy' },
        { id: 3, name: 'Color Code Convertor', color: '#FF9454', href: 'https://codepen.io/yejun614/pen/dyNjdeb' },
        { id: 4, name: 'Algorithm', color: '#E8704D', href: 'https://github.com/yejun614/algorithm-solve' },
        { id: 5, name: 'Arduino Education', color: '#F25C05', href: 'https://github.com/yejun614/Arduino-Structure-and-Design' },
        { id: 5, name: 'My Highlight', color: '#92C0A0', href: 'https://yejun614.github.io/my-highlight/' },
        { id: 5, name: 'Fuzzy Cluster Means', color: '#519B68', href: 'https://github.com/yejun614/fuzzy-cluster-means' },
        { id: 5, name: 'Genetic Algorithm', color: '#306D43', href: 'https://github.com/yejun614/genetic-algorithm-example' }
      ]
    }
  },
  methods: {
    async showDocument (page) {
      /*
      const data = await this.$content(page).fetch()
      console.log(page, data)
      */
    }
  }
}
</script>

<style>
  #my-works .cover {
    display: grid;
    grid-template-columns: 1fr;
  }

  #my-works .cover .box {
    width: 300px;
    height: 30px;
    padding: 20px;
    margin: 10px;

    background-color: #333;
    border-radius: 10px;

    color: white;
    font-size: 15px;
    font-weight: bold;
    text-align: center;
    text-decoration: blink;

    display: flex;
    align-items: center;
    justify-content: center;

    transition: box-shadow 300ms ease-in-out;
  }

  #my-works .cover .box:hover {
    box-shadow: 3px 3px 12px rgba(0,0,0,.5);
  }

  @media screen and (min-width: 600px) {
    #my-works .cover {
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr 1fr;
    }

    #my-works .cover .box {
      width: 180px;
      height: 180px;
      border-radius: 20px;

      font-size: 15px;
    }
  }

  @media screen and (min-width: 1000px) {
    #my-works .cover {
      grid-template-columns: 1fr 1fr 1fr;
    }
  }
</style>
