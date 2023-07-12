<script setup>
// submitForm needs to be handled down here
const submitForm = () => {

  // disable the button to prevent double submission
  document.querySelector('#pasteit').disabled = true

  // grab the title from the input
  const title = document.getElementById('title').value

  // grab the content from the textarea
  const body = document.getElementById('body').value

  // post the content to the api
  fetch('https://szsaextmvibiosujacix.supabase.co/functions/v1/paste', {
    method: 'POST',
    body: JSON.stringify({
      title: title,
      body: body
    })
  })
    // redirect to the new paste
    .then(res => res.json())
    .then(data => {
      // console.log(data)
      window.location.href = `/#/p/${data[0].uuid}`
    }).catch(err => {

      // disable the button to prevent double submission
      document.querySelector('#pasteit').disabled = false

      console.error(err)
    })
}
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
      <input type="text" name="title" id="title" style="font-family: monospace; font-size: 16px;" />
    </p>
    <p>
      <label for="body">Paste</label>
      <textarea name="body" id="body" rows="10" style="font-family: monospace; font-size: 16px;"></textarea>
    </p>
    <p><button data-tooltip="Let's go!" id="pasteit" @click.prevent="submitForm">Make Pasta 🍝</button></p>
  </article>
</template>
