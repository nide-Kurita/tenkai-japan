<script lang="ts" setup>
const search = ref("");

const results = searchContent(search);
</script>

<template>
  <main>
    <!-- <input v-model="search">
    <pre>{{ results }} </pre> -->
    <!-- <ContentDoc/> -->
    <div></div>
    <header class="header">
      <div class="cmn-inner">
        <p class="logo">
          <img src="/img/logo.jpg" alt="">
        </p>
      </div>
    </header>
    <ContentDoc v-slot="{ doc }">
      <article>
        <div class="content">
          <div class="cmn-inner">
            <h1>{{ doc.title }}</h1>

            <ContentRenderer :value="doc" />
          </div>
        </div>
      </article>
    </ContentDoc>
  </main>
</template>

<style>
.content {
}
.cmn-inner {
  max-width: 1020px;
  margin: 0 auto;
  padding: 0 40px;
}

.header {
  background-color: #e08698;
}

.header img {
  width: 150px;
}

.logo {
  margin: 0;
}

h1 {
  font-size: 42px;
  border-bottom: 1px solid #000;
}

img {
  width: 100%;
}




</style>

