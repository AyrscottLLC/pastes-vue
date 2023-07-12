<template>
  <div>
    <link href="https://cdn.jsdelivr.net/npm/@picocss/pico@1.5.10/css/pico.min.css" rel="stylesheet">
    <div class="container">
      <nav>
        <ul>
          <li>pastes-vue.ayrscott.com 🍝</li>
        </ul>
        <ul>
          <li>
            <RouterLink to="/">Home</RouterLink>
          </li>
          <li>
            <RouterLink to="/about">About</RouterLink>
          </li>
          <li>
            <RouterLink to="/p/63de90ba-3d13-45e6-98f9-8ec4ae8638fd">Sample</RouterLink>
          </li>
        </ul>
      </nav>
    </div>


    <main class="container">
      <router-view :key="$route.fullPath" />
    </main>



    <footer class="container">
      <article>
        <small>Copyright ©️ 2023 Ayrscott, LLC</small>
      </article>
    </footer>
  </div>
</template>

<script setup>
</script>

<style scoped></style>
