<template>
  <section id="my-profile">
    <h1>WHO IS YEJUN</h1>

    <div class="card" :class="{flip: isFlip}" @click="flipping()">
      <table class="front">
        <tr>
          <td>E-Mail</td>
          <td>yejun614@naver.com</td>
        </tr>

        <tr>
          <td>학교</td>
          <td>동의대학교 응용소프트웨어공학 전공 2학년 재학</td>
        </tr>

        <tr>
          <td>좋아하는 것</td>
          <td>캠핑가서 힐링하기.</td>
        </tr>

        <tr>
          <td>관심 분야</td>
          <td>웹 개발, 게임 개발, 클라우드, 인공지능</td>
        </tr>
      </table>

      <div class="back">
        <span>I am YEJUN, JUNG !</span>
      </div>
    </div>

    <div class="messages">
      <p>코딩을 좋아하는 평범한 대학생 입니다.</p>
      <p>새로운 기술을 공부할 때는 항상 토이 프로젝트를 만들어서 실제로 적용해보는 편입니다.</p>
    </div>

    <div class="click-me">
      <span class="text">Click Me</span>
      <img class="arrow-img" src="arrow.png">
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyProfile',
  data () {
    return {
      isFlip: false
    }
  },
  methods: {
    flipping () {
      this.isFlip = !this.isFlip
    }
  }
}
</script>

<style>
  @keyframes click-me-rotate {
    from { transform: rotate(-30deg); }
    50%  { transform: rotate(-20deg); }
    to   { transform: rotate(-30deg); }
  }

  #my-profile {
    perspective: 600px;
    /* position: relative; */
  }

  #my-profile .card {
    cursor: pointer;

    transform-style: preserve-3d;
    transform-origin: center right;
    transition: transform 300ms ease-in-out;

    position: relative;
  }

  #my-profile .card:hover {
    transform: translateX(-10px) rotateY(-10deg);
  }

  #my-profile .card.flip {
    transform: translateX(-100%) rotateY(-180deg);
  }

  #my-profile table {
    border-radius: 20px;
    background-color: white;

    background: rgb(91,160,255);
    background: linear-gradient(45deg, rgba(91,160,255,1) 0%, rgba(255,161,161,1) 100%);

    color: white;

    padding: 30px 10px;
    backface-visibility: hidden;
    box-shadow: 3px 5px 10px rgba(0,0,0,.3);
  }

  #my-profile td {
    padding: 2px 10px;
    font-weight: bold;
    font-size: 12px;
  }

  #my-profile .back {
    position: absolute;
    top: 0;
    left: 0;

    width: 100%;
    height: 100%;
    background-color: midnightblue;
    transform: rotateY( 180deg );
    backface-visibility: hidden;
    border-radius: 20px;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

  }

  #my-profile .back span {
    color: white;
    font-size: 15px;
    font-weight: bold;

    padding: 2px 5px;
    border-bottom: 2px solid white;
  }

  #my-profile .messages {
    width: 80%;
    margin-top: 100px;
  }

  #my-profile .messages p {
    color: #777;
    font-size: 12px;
    text-align: center;

    padding: 3px 0;
  }

  .click-me {
    display: none;
    animation: click-me-rotate 1s infinite;
  }

  .click-me .arrow-img {
    width: 150px;
  }

  .click-me .text {
    display: inline-block;
    font-size: 15px;
    font-weight: bold;
    text-align: center;

    transform: rotate(50deg) translate(15px, -10px);
  }

  @media screen and (min-width: 600px) {
    #my-profile td {
      padding: 3px 12px;
      font-size: 15px;
    }

    #my-profile .messages p {
      font-size: 15px;
    }
  }

  @media screen and (min-width: 800px) {
    .click-me {
      display: inline;
      position: absolute;
      top: 250px;
      margin-right: 630px;
    }

    .click-me .arrow-img {
      width: 100px;
    }
  }

  @media screen and (min-width: 1000px) {
    #my-profile td {
      padding: 5px 30px;
      font-size: 17px;
    }

    #my-profile .messages p {
      font-size: 20px;
    }

    .click-me {
      margin-right: 800px;
    }
  }
</style>
