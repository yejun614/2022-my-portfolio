<template>
  <section id="my-skills">
    <h1>
      기술 스택
    </h1>

    <div ref="badge" class="badge" />

    <div class="tech">
      <img class="trophy" src="https://github-profile-trophy.vercel.app/?username=yejun614" alt="trophy">
      <img class="stats" src="https://github-readme-stats.vercel.app/api?username=yejun614&show_icons=true" alt="stats">
      <img class="top-langs" src="https://github-readme-stats.vercel.app/api/top-langs/?username=yejun614&show_icons=true&hide_border=true&title_color=004386&icon_color=004386&layout=compact" alt="top-langs">

      <a class="solved" href="https://solved.ac/profile/yejun614" target="_blink">
        <img src="https://mazassumnida.wtf/api/v2/generate_badge?boj=yejun614" alt="boj badge">
      </a>
    </div>

    <div class="links">
      <a href="https://github.com/yejun614" target="_blink">Github Profile</a>
      <a href="https://solved.ac/profile/yejun614" target="_blink">Solved.ac Profile</a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MySkills',
  data () {
    return {
      skills: [
        { name: 'python', hex: '306998', logo: 'python' },
        { name: 'go', hex: '29BEB0', logo: 'go' },
        { name: 'javascript', hex: 'F0DB4F', logo: 'javascript' },
        { name: 'typescript', hex: '007acc', logo: 'typescript' },
        { name: 'cplusplus', hex: '044F88', logo: 'cplusplus' },
        { name: 'amazon%20aws', hex: 'FF9900', logo: 'amazon%20aws' },
        { name: 'vercel', hex: '000000', logo: 'vercel' },
        { name: 'unity', hex: '222c37', logo: 'unity' },
        { name: 'flask', hex: '333333', logo: 'flask' },
        { name: 'vue.js', hex: '41B883', logo: 'vue.js' },
        { name: 'nuxt.js', hex: '35495E', logo: 'nuxt.js' }
      ]
    }
  },
  mounted () {
    const element = this.$refs.badge

    this.skills.forEach((skill) => {
      const badge = document.createElement('img')
      badge.src = `https://img.shields.io/badge/${skill.name}-${skill.hex}?style=for-the-badge&logo=${skill.logo}&logoColor=white`

      element.appendChild(badge)
    })
  }
}
</script>

<style>
  #my-skills .badge {
    width: 90%;
    margin-bottom: 50px;
    text-align: center;
  }

  #my-skills .tech {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .tech img {
    max-width: 90%;
    margin: 20px 0;
  }

  .trophy {
    display: none;
  }

  #my-skills .links {
    margin-top: 50px;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  #my-skills .links a {
    color: coral;
    font-size: 12px;
    font-weight: bold;
    text-decoration: blink;

    padding: 5px 10px;
    margin: 5px 0;
    border: 3px solid coral;
    border-radius: 5px;

    transition: all 300ms ease-in-out;
  }

  #my-skills .links a:hover {
    color: white;
    background-color: coral;
  }

  @media screen and (min-width: 600px) {
    .tech img {
      max-width: 400px;
    }

    .trophy {
      display: inline;
    }

    #my-skills .links a {
      font-size: 15px;
    }
  }

  @media screen and (min-width: 1000px) {
    .tech img {
      max-width: 800px;
    }

    #my-skills .badge {
      width: 800px;
    }

    #my-skills .links a {
      font-size: 17px;
    }
  }
</style>
