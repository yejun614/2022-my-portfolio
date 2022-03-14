<template>
  <section id="footer">
    <div class="info">
      <div class="icons">
        <a href="https://github.com/yejun614" target="_blink">
          <i class="im im-github" aria-hidden="true" />
        </a>
      </div>

      <h3>coltoge.com</h3>
      <p>&copy; Copyright 2022 YeJun, Jung All rights reserved.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SiteFooter'
}
</script>

<style>
  #footer {
    height: 200px;
    margin: 250px 0 0 0 !important;
    padding-top: 100px;

    background: #3B82BF;
  }

  #footer .info {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }

  #footer .info .icons a {
    color: white;
  }

  #footer .info h3 {
    color: rgba(255,255,255,.5);
    font-weight: normal;
    margin-top: 50px;
    margin-bottom: 10px;
  }

  #footer p {
    color: rgba(255,255,255,.8);
    font-size: 12px;
  }

  @media screen and (min-width: 1000px) {
    .waves {
      max-height: 150px;
    }
  }

  @media screen and (min-width: 1000px) {
    .waves {
      max-height: 180px;
    }
  }
</style>
