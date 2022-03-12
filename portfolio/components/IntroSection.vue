<template>
  <div id="intro-section">
    <div class="background-video">
      <iframe
        ref="background"
        src=""
        frameborder="0"
        allow="autoplay; fullscreen"
        allowfullscreen
      />
    </div>

    <div id="logo">
      <ColtogeLogo />
    </div>

    <div id="welcome-typing">
      <TypingAnim
        text="Hello!\nI'm YeJun and Software Engineer."
        :speed="50"
        :delay="2000"
      />
    </div>

    <div class="scroll">
      <ScrollDown />
    </div>
  </div>
</template>

<script>
export default {
  name: 'IntroSection',
  data () {
    return {
      backgroundVideoes: [
        'https://player.vimeo.com/video/626985671?background=1&autoplay=1&loop=1&transparent=1',
        'https://player.vimeo.com/video/416330739?background=1&autoplay=1&loop=1&transparent=1',
        'https://player.vimeo.com/video/447087612?background=1&autoplay=1&loop=1&transparent=1',
        'https://player.vimeo.com/video/592491784?background=1&autoplay=1&loop=1&transparent=1',
        'https://player.vimeo.com/video/548671139?background=1&autoplay=1&loop=1&transparent=1',
        'https://player.vimeo.com/video/626004752?background=1&autoplay=1&loop=1&transparent=1'
      ],
      backgroundSpeed: 10000,
      currentBackground: -1
    }
  },
  mounted () {
    this.nextVideo()
  },
  methods: {
    nextVideo () {
      this.currentBackground++
      this.currentBackground %= this.backgroundVideoes.length

      this.$refs.background.src = this.backgroundVideoes[this.currentBackground]
    }
  }
}
</script>

<style>
  @keyframes fade-in {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  #intro-section {
    width: 100%;
    height: 100%;

    display: flex;
    align-items: center;
    justify-content: center;

    position: absolute;
  }

  .background-video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    pointer-events: none;
    overflow: hidden;

    opacity: 0;
    animation: fade-in 1s forwards 4s;
  }

  .background-video iframe {
    /* https://codepen.io/abennington/pen/ezaPPy?editors=1100 */
    width: 100vw;
    height: 56.25vw;
    min-height: 100vh;
    min-width: 177.77vh;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  #logo {
    position: absolute;
    top: 5px;
    left: 13px;
  }

  #welcome-typing {
    width: 300px;
    height: 150px;

    display: flex;
    align-items: center;
    justify-content: center;

    color: coral;
    font-size: 12px;
    font-weight: bold;
    text-align: center;

    /* From https://css.glass */
    background: rgba(255, 255, 255, 0.2);
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5px);
    border: 1px solid rgba(255, 255, 255, 0.3);
  }

  .scroll {
    position: absolute;
    bottom: 25px;
    left: 50%;
    margin-left: -30px;

    opacity: 0;
    animation: fade-in 1s forwards 4s;
  }

  @media screen and (min-width: 600px) {
    #welcome-typing {
      width: 600px;
      height: 200px;
      font-size: 20px;
    }

    .scroll {
      margin-left: -40px;
    }
  }

  @media screen and (min-width: 1000px) {
    #welcome-typing {
      width: 800px;
      height: 300px;
      font-size: 30px;
    }

    .scroll {
      margin-left: -57px;
    }
  }
</style>
