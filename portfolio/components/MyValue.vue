<template>
  <section id="my-value">
    <h1>
      관심 분야
    </h1>
  </section>
</template>

<script>
export default {
  name: 'MyValue',
  data () {
    return {
      items: [
        { id: 0, image: '', title: '', content: '' },
        { id: 1, image: '', title: '', content: '' },
        { id: 2, image: '', title: '', content: '' },
        { id: 3, image: '', title: '', content: '' }
      ]
    }
  }
}
</script>

<style>
  #my-value {
    padding-top: 0;
  }
</style>
