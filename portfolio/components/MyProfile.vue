<template>
  <section id="my-profile">
    <h1>WHO IS YEJUN</h1>

    <table>
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
        <td>싫어하는 것</td>
        <td>무책임한 사람.</td>
      </tr>
    </table>

    <div class="messages">
      <p>코딩을 좋아하는 평범한 대학생 입니다.</p>
      <p>새로운 기술을 공부할 때는 항상 토이 프로젝트를 만들어서 실제로 적용해보는 편입니다.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyProfile'
}
</script>

<style>
  #my-profile table {
    border: 3px solid black;
    padding: 10px;
  }

  #my-profile td {
    padding: 5px 30px;
    font-weight: bold;
    font-size: 17px;
  }

  #my-profile .messages {
    margin-top: 100px;
  }

  #my-profile .messages p {
    font-size: 20px;
    font-weight: bold;
    text-align: center;

    padding: 3px 0;
  }
</style>
