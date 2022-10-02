<template>
  <div class="x-container">
    <div class="profile-title">
      <iconMain class="icon" name="avatarMin" />
      <div class="profile-name">joshua_l</div>
    </div>
    <div class="user__post-container">
      <slot name="userPost" />
    </div>
    <div class="reviews">
      <togglerReviews @onToggle="toggle" />
      <div class="comments" v-if="shown">
        <ul class="comments-list">
          <li class="comments-item" v-for="n in 5" :key="n">
            <commentProfile text="nice app dude" username="john" />
          </li>
        </ul>
      </div>
    </div>
    <div class="date">15 may</div>
  </div>
</template>
<script>
import { iconMain } from '../../icons'
import { togglerReviews } from '../togglerReviews'
import { commentProfile } from '../commentProfile'

export default {
  components: {
    iconMain,
    togglerReviews,
    commentProfile
  },
  data () {
    return {
      shown: false
    }
  },
  methods: {
    toggle (isOpened) {
      this.shown = isOpened
    }
  }
}
</script>
<style lang="scss" src="./userProfile.scss" scoped>

</style>
