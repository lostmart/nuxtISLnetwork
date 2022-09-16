<template>
  <div class="container">
    <h2 class="text-center">FAQ</h2>
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Title 01</h5>
        <iframe
          src="https://player.vimeo.com/video/750506521?h=cd8fb2e8f0"
          frameborder="0"
          allow="autoplay; fullscreen; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>
    <div class="card">
      <div class="card-body">
        <h5 class="card-title">Title 02</h5>
        <div style="padding: 75% 0 0 0; position: relative">
          <iframe
            src="https://player.vimeo.com/video/750515103?h=828ee6e1f2&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479"
            frameborder="0"
            allow="autoplay; fullscreen; picture-in-picture"
            allowfullscreen
            style="
              position: absolute;
              top: 0;
              left: 0;
              width: 100%;
              height: 100%;
            "
            title="Voces -2"
          ></iframe>
        </div>
        <script src="https://player.vimeo.com/api/player.js"></script>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "ISL network voces",
    };
  },
  head() {
    return {
      title: this.title,
    };
  },
};
</script>
<style scoped>
.card {
  max-width: 650px;
  margin: auto;
}
iframe {
  width: 100%;
  margin: auto;
  min-height: 200px;
}
</style>
