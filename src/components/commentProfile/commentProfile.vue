<template>
  <div class="c-comment">
    <p>
      <span class="username">{{username}}</span>
      {{ text }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'commentProfile',
  props: {
    username: {
      type: String,
      required: true
    },
    text: {
      type: String,
      required: true
    }
  }
}
</script>
<style lang="scss" src="./commentProfile.scss" scoped></style>
