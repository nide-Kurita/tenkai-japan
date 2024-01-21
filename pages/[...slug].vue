<script lang="ts" setup>
const search  = ref('')

const results = searchContent(search)

</script>

<template>
  <main>
    <!-- <input v-model="search">
    <pre>{{ results }} </pre> -->
    <!-- <ContentDoc/> -->
    <ContentDoc v-slot="{ doc }">
      <article>
        <h1>{{ doc.title }}</h1>
        <ContentRenderer :value="doc" />
      </article>
    </ContentDoc>
    
  </main>
</template>


