<template>
  <section id="my-value">
    <h1>
      가치관
    </h1>

    <div class="cover">
      <div class="box" style="background: #FFB5A6;">
        <span class="num">1.</span>
        <span>기본을 지킵니다</span>
      </div>

      <div class="box" style="background: #FF9683;">
        <span class="num">2.</span>
        <span>사용자 경험을 함께 생각합니다</span>
      </div>

      <div class="box" style="background: #FF9683;">
        <span class="num">3.</span>
        <span>혼자 뛰어 가지 말고, <br>동료들과 함께 걸어갑니다</span>
      </div>

      <div class="box" style="background: #FF775F;">
        <span class="num">4.</span>
        <span>실패를 두려워하지 않고, <br>끊임없이 새로운 것에 도전합니다</span>
      </div>
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
    padding-top: 0;
  }

  #my-value .cover {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
  }

  #my-value .box {
    width: 150px;
    height: 150px;

    padding: 10px;
    margin: 10px;
    border-radius: 20px;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;

    background-color: white;
    color: #F2F0E9;
  }

  #my-value .box span {
    font-size: 12px;
  }

  #my-value .box .num {
    font-size: 25px;
    margin: 10px 0;
  }

  @media screen and (min-width: 600px) {
    #my-value .box {
      width: 200px;
      height: 200px;
    }

    #my-value .box span {
      font-size: 14px;
    }
  }

  @media screen and (min-width: 1000px) {
    #my-value .box {
      width: 250px;
      height: 250px;
    }

    #my-value .box span {
      font-size: 15px;
    }
  }
</style>
