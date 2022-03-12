<template>
  <section id="footer">
    <h3>coltoge.com</h3>

    <div class="icons">
      <a href="https://github.com/yejun614" target="_blink">
        <i class="im im-github" aria-hidden="true" />
      </a>
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
    min-height: fit-content;

    background-color: #333;
    margin-bottom: 0 !important;

    justify-content: space-between;
    padding: 100px 0;
  }

  #footer h3 {
    color: #555;
  }

  #footer .icons a {
    color: white;
  }

  #footer h3 {
    margin-bottom: 50px;
  }
</style>
