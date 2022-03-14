<template>
  <div class="coltoge-logo">
    <a href="https://coltoge.com">
      coltoge.com
    </a>
  </div>
</template>

<script>
export default {
  name: 'ColtogeLogo'
}
</script>

<style>
  .coltoge-logo {
    width: fit-content;
    height: 20px;
    padding: 3px 20px;
    margin: 10px;
    border-radius: 7px;
    cursor: pointer;

    display: flex;
    align-items: center;
    justify-content: center;

    transition: background-color 300ms ease;
  }

  .coltoge-logo a {
    font-size: 10px;
    color: coral;
    text-decoration: blink;
  }

  @media screen and (min-width: 600px) {
    .coltoge-logo a {
      font-size: 12px;
    }
  }

  @media screen and (min-width: 1000px) {
    .coltoge-logo a {
      font-size: 15px;
    }
  }
</style>
