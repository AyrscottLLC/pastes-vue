<template>
    <div>
        <article>
            <hgroup>
                <h1>About</h1>
                <h2>pastes-vue</h2>

            </hgroup>

            <p>This is a portfolio project demonstrating full stack competency with a collection of technologies
                including DNS, Vue 3, GitHub Pages, Tailwind CSS, Supabase & PostgreSQL.</p>


            <p>The full source code for this project is available on GitHub:</p>
            <ul>
                <li>
                    <a href="https://github.com/AyrscottLLC/pastes-vue">Vue 3 Front-End for GitHub Pages</a>
                </li>
                <li>
                    <a href="https://github.com/AyrscottLLC/pastes-supabase">Deno Edge Functions Back-End for
                        Supabase</a>
                </li>
            </ul>
        </article>

        <section aria-label="subscribe">
            <div class="container">
                <article>
                    <hgroup>
                        <h2>Subscribe</h2>
                        <h3>Get the latest pasta updates</h3>
                    </hgroup>
                    <form class="grid">
                        <input type="text" id="name" name="name" placeholder="Your name" aria-label="Your name" required />
                        <input type="email" id="email" name="email" placeholder="Email address" aria-label="Email address"
                            required />
                        <button type="submit" onclick="event.preventDefault()">Subscribe</button>
                    </form>
                </article>
            </div>
        </section>
    </div>
</template>

<script setup>
</script>

<style scoped></style>
