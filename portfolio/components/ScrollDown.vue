<template>
  <div class="scroll-down">
    <span>PORTFOLIO</span>
    <img class="arrow-down" src="icons/arrow-down.png">
  </div>
</template>

<script>
export default {
  name: 'ScrollDown'
}
</script>

<style>
  @keyframes scroll-anim {
    from, 24%, 50% { margin-bottom: 0; }
    12%, 36% { margin-bottom: 10px; }
  }

  .scroll-down {
    font-size: 10px;
    font-weight: bold;
    color: coral;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    animation: scroll-anim 1s infinite ease-in-out;
  }

  .scroll-down > * {
    margin: 5px 0;
  }

  .arrow-down {
    width: 10px;
  }

  @media screen and (min-width: 600px) {
    .scroll-down {
      font-size: 15px;
    }

    .arrow-down {
      width: 15px;
    }
  }

  @media screen and (min-width: 1000px) {
    .scroll-down {
      font-size: 20px;
    }

    .arrow-down {
      width: 20px;
    }
  }
</style>
