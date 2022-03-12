<template>
  <section id="my-value">
    <h1>
      도전의 가치를 중요하게 생각합니다.
    </h1>

    <div class="box">
      <img src="https://images.unsplash.com/photo-1597892657493-6847b9640bac?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1287&q=80" alt="marathon">
      <p>
        프로그래밍은 도전과 실패 그리고 약간의 성공이 반복되는 마라톤이라고 생각합니다.
      </p>
    </div>

    <div class="box reverse">
      <img src="https://images.unsplash.com/photo-1577493327436-6b54af0aabb3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=927&q=80" alt="castle">

      <p>
        수많은 실패와 경험들이 쌓여서 만들어진 성벽은 견고해서 적군의 공격을 막아내는데 탁월합니다.
      </p>
    </div>

    <div class="box">
      <img src="https://images.unsplash.com/photo-1581090465357-c8a1f71f0407?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1287&q=80" alt="tech">

      <p>
        공학도 이와 다르지 않다고 생각합니다. 실패를 통해서 새로운 배움을 얻고, 이러한 경험들은 더욱 빈틈없는 솔루션을 만들어 내는 지지대가 되어 줍니다.
      </p>
    </div>

    <div class="messages">
      <p>기본을 지킵니다.</p>
      <p>사용자 디자인을 함께 생각합니다.</p>
      <p>혼자 뛰어 가지 말고, 동료들과 함께 걸어갑니다.</p>
      <p>실패를 두려워하지 않고, 끊임없이 새로운 것에 도전합니다.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MyValue'
}
</script>

<style>
  #my-value {
    padding-top: 100px;
  }

  #my-value .box {
    margin: 20px 0;
  }

  #my-value .box img {
    width: 400px;
    position: relative;
    right: 50px;
    border: 3px solid black;
    padding: 20px;
  }

  #my-value .box p {
    width: 500px;
    padding: 20px 30px;

    font-size: 20px;

    background-color: white;
    border: 3px solid black;

    position: relative;
    bottom: 180px;
    left: 150px;
  }

  #my-value .box.reverse img {
    right: 0;
    left: 250px;
  }

  #my-value .box.reverse p {
    left: 0;
    bottom: 300px;
  }

  #my-value .messages p {
    color: rgba(0,0,0,.3);
    font-size: 20px;
    font-weight: bold;
    text-align: center;
    padding: 15px 0;
    letter-spacing: 1.5px;
    word-spacing: 5px;
    cursor: pointer;
    transition: color 300ms ease-in-out;
  }

  #my-value .messages p:hover {
    color: black;
  }
</style>
