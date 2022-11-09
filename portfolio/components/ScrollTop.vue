<template>
  <a id="scroll-top" href="#intro">
    <img class="arrow-up" src="icons/arrow-up.png">
  </a>
</template>

<script>
export default {
  name: 'ScrollTop'
}
</script>

<style>
  @keyframes fade-in {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  #scroll-top {
    width: 40px;
    height: 40px;
    background-color: coral;
    border: 5px solid coral;
    opacity: 0;

    position: fixed;
    right: 30px;
    bottom: 30px;

    display: flex;
    align-items: center;
    justify-content: center;

    text-decoration: blink;
    transition: all 300ms ease-in-out;
    animation: fade-in 300ms forwards;
  }

  #scroll-top:hover {
    background-color: rgba(0,0,0,0);
  }

  #scroll-top .arrow-up {
    width: 80%;
    filter: grayscale(1) brightness(0) invert(1);

    transition: color 300ms ease-in-out;
  }

  #scroll-top:hover .arrow-up {
    filter: invert(0);
  }
</style>
