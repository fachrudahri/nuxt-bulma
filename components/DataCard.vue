<template>
    <div class="column is-4">
      <div class="card">
        <div class="card-content">
          <div class="media">
            <div class="media-left">
              <figure class="image">
                <img src="https://bulma.io/images/placeholders/96x96.png" alt="Placeholder image" />
              </figure>
            </div>
            <div class="media-content">
              <p class="title is-4">{{ name }}</p>
              <p class="subtitle is-6 mt-5">@{{ username }}</p>
              <p class="subtitle is-6">{{ email }}</p>
              <p class="subtitle is-6">{{ phone }}</p>
            </div>
          </div>

          <div class="content">
            <a :href="website">{{ website }}</a>
            <a href="#">#responsive</a>
            <br />
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'DataCard',
  props: {
    name: {
      type: String,
      required: true
    },
    username: {
      type: String,
      required: true
    },
    email: {
      type: String,
      required: true
    },
    phone: {
      type: String,
      required: true
    },
    website: {
      type: String,
      required: true
    }
  }

};
</script>

<style>
</style>
