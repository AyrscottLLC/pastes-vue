<script setup>
</script>

<template>
  <article>
    <hgroup>
      <h1>Greetings</h1>
      <h2>Welcome to pastes-vue.ayrscott.com</h2>

    </hgroup>

    <p>Another place to share the latest and greatest in all things copy pasta! 🍝</p>

    <p>
      <label for="title">Paste Title</label>
      <input type="text" name="title" id="title" />
    </p>
    <p>
      <label for="body">Paste</label>
      <textarea name="body" id="body" rows="10"></textarea>
    </p>
    <p><button data-tooltip="Let's go!">Make Pasta 🍝</button></p>
  </article>
</template>
