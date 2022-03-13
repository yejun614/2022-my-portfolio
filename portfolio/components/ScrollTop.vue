<template>
  <a id="scroll-top" href="#intro">
    <i class="im im-care-up" aria-hidden="true" />
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
    border: 3px solid coral;
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

  #scroll-top .im {
    color: white;
    font-size: 17px;

    transition: color 300ms ease-in-out;
  }

  #scroll-top:hover .im {
    color: coral;
  }
</style>
