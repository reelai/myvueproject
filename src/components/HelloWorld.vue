<script setup lang="ts">
defineProps<{
  msg: string
  isButtonDisabled: boolean
}>()
</script>

<template>
  <!-- 这个一个整体div, 里面的block元素自然是竖着排-->
  <div class="greetings">
    <h1 class="green">{{ msg + "<h1>h2</h1>" }}</h1>
    <h3>
      You have successfully created a project with
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>. What's next?
       <hr/>
      <button :disabled="isButtonDisabled">Button</button>
      <span>myspan</span>
      <p>{{ msg.length}} {{ msg }}</p>
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
