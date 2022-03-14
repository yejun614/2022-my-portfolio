<template>
  <section id="my-value">
    <h1>
      가치관
    </h1>

    <div class="cover">
      <div class="box" style="background: #FFB5A6;">
        <span>기본을 지킵니다.</span>
      </div>

      <div class="box" style="background: #FF9683;">
        <span>사용자 경험을 함께 생각합니다.</span>
      </div>

      <div class="box" style="background: #FF9683;">
        <span>혼자 뛰어 가지 말고, <br>동료들과 함께 걸어갑니다.</span>
      </div>

      <div class="box" style="background: #FF775F;">
        <span>실패를 두려워하지 않고, <br>끊임없이 새로운 것에 도전합니다.</span>
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
    width: 250px;
    height: 250px;

    padding: 10px;
    margin: 10px;
    border-radius: 20px;

    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;

    background-color: white;
    color: #F2F0E9;
  }

  #my-value .box span {
    font-size: 15px;
  }
</style>
