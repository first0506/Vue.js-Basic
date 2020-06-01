<template>
  <div>
      <h1></h1>
      <ul>
          <li v-for="video in videos" :key="video.etag">
              {{ video.snippet.description }}
          </li>
      </ul>
  </div>
</template>

<script>
export default {
    name: 'VideoList',
    props: {
        videos: Array,
    }
}
</script>

<style>

</style>