<template>
  <div class="scroll-down">
    <span>PORTFOLIO</span>
    <i class="im im-angle-down" aria-hidden="true" />
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

  @media screen and (min-width: 600px) {
    .scroll-down {
      font-size: 15px;
    }
  }

  @media screen and (min-width: 1000px) {
    .scroll-down {
      font-size: 20px;
    }
  }
</style>
