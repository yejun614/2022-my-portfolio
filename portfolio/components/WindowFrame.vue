<template>
  <div class="window-frame">
    <div class="window-title">
      <span class="title">
        {{ title }}
      </span>
    </div>

    <div class="window-body">
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  name: 'WindowFrame',
  props: {
    title: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped>
  .window-frame {
    min-width: 100px;
    min-height: 100px;
    background-color: rgba(0,0,0,.3);
    border: 3px solid black;
    border-radius: 5px;
  }

  .window-title {
    width: 100%;
    height: 35px;
    border-bottom: 3px solid black;
  }

  .title {
    font-size: 15px;
    font-weight: bold;
    padding: 0 20px;
  }

  .window-body {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
</style>
