<template>
  <div id="layout">
    <div id="intro">
      <IntroSection />
    </div>

    <content>
      <header>
        <TopNav />
      </header>

      <MyProfile />
      <MyWorks />
      <MySkills />

      <SiteFooter />

      <ScrollTop v-if="isScrollTop" />
    </content>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      isScrollTop: false
    }
  },
  mounted () {
    document.addEventListener('scroll', () => this.scrolling())
  },
  methods: {
    scrolling () {
      const scrollY = window.scrollY

      if (scrollY > window.innerHeight / 2) {
        this.isScrollTop = true
      } else {
        this.isScrollTop = false
      }
    }
  }
}
</script>

<style>
  @keyframes fade-in {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  * {
    margin: 0;
    padding: 0;
  }

  html, body {
    padding: 0;
    margin: 0;
    font-family: 'Noto Sans KR', sans-serif;
    scroll-behavior: smooth;
  }

  #layout section {
    width: 100%;
    margin: 100px 0;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
  }

  #layout section h1 {
    color: coral;
    text-align: center;
    font-size: 16px;
    padding: 5px 3px;
    border-bottom: 3px solid coral;
    margin-bottom: 50px;
  }

  #intro, content {
    width: 100%;
    min-height: 100%;
    margin: 0;
    padding: 0;

    position: absolute;
    top: 0;
    left: 0;

    animation: fade-in 1s forwards;
  }

  content {
    top: 100%;
    background-color: #f3f8ff;
  }

  content section {
    margin-top: 300px;
  }

  header {
    width: 100%;
    height: 70px;
    background-color: coral;

    position: sticky;
    top: 0;
    left: 0;

    display: flex;
    align-items: center;
    justify-content: center;

    z-index: 100;
  }

  @media screen and (min-width: 600px) {
    #layout section h1 {
      font-size: 18px;
      margin-bottom: 80px;
    }
  }

  @media screen and (min-width: 1000px) {
    #layout section h1 {
      font-size: 25px;
      margin-bottom: 100px;
    }
  }
</style>
