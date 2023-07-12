<script setup>
import { ref } from 'vue'

const { id } = defineProps(['id'])

const paste = ref(null)

const api_url = 'https://szsaextmvibiosujacix.supabase.co/functions/v1/get_paste_by_uuid'

const requestOptions = {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ uuid: id }),
    id: id,
    key: id
};

fetch(api_url, requestOptions)
    .then(response => response.json())
    .then(data => {
        // check for an error and redirect to home page
        if (data.error) {
            console.error('Error:', data.error);
            window.location.href = '/'
        }

        // otherwise, set the paste data
        paste.value = data.data
    }).catch((error) => {
        console.error('Error:', error);
        window.location.href = '/'
    })




</script>

<template>
    <article>
        <hgroup>
            <h1>{{ paste?.title }}</h1>
            <h2><em>paste {{ id }}</em></h2>
        </hgroup>

        <pre>{{ paste?.body }}</pre>
    </article>
</template>
