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
    font-size: 8px;
    color: coral;
    text-decoration: blink;
  }

  .coltoge-logo:hover {
    background-color: coral;
  }

  .coltoge-logo:hover a {
    color: white;
  }

  @media screen and (min-width: 600px) {
    .coltoge-logo {
      height: 25px;
      padding: 3px 10px;
      margin: 10px;
    }

    .coltoge-logo a {
      font-size: 12px;
    }
  }

  @media screen and (min-width: 1000px) {
    .coltoge-logo {
      height: 30px;
      padding: 3px 20px;
      margin: 20px;

      border: 3px solid coral;
    }

    .coltoge-logo a {
      font-size: 15px;
    }
  }
</style>
