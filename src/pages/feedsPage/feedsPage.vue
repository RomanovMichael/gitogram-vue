<template>
  <div class="topline">
    <topLine>
      <template #headline>
        <h1>Gitogram /</h1>
        <div class="navigation">
          <iconMain class="icon" name="homeHeader" />
          <iconMain class="icon" name="avatarMin" />
          <iconMain class="icon" name="exitHeader" />
        </div>
      </template>
      <template #content>
        <ul class="stories">
          <li class="stories-item" v-for="story in stories" :key="story.id">
            <storyUseritem :avatar="story.avatar" :username="story.username" />
          </li>
        </ul>
      </template>
    </topLine>
  </div>
  <div class="userProfile">
    <userProfile>
      <template #userPost>
        <div class="user__post-content">
          <div class="user__post-title">Vue.js</div>
          <div class="user__post-desc">
            <span><b>JavaScript</b></span> framework for building interactive web applications ⚡
          </div>
          <div class="ratings__wrap">
            <div class="ratings__item">
              <iconMain class="ratings__item-icon" name="ratingsStar" />
              <div class="ratings__item-title">Star</div>
            </div>
            <div class="ratings__item">
              <div class="ratings__item-title">156k</div>
            </div>
            <div class="ratings__item">
              <iconMain class="ratings__item-icon" name="ratingsFork" />
              <div class="ratings__item-title">Fork</div>
            </div>
            <div class="ratings__item">
              <div class="ratings__item-title">4</div>
            </div>
          </div>
        </div>
      </template>
    </userProfile>
  </div>

  <div class="userProfile">
    <userProfile>
      <template #userPost>
        <div class="user__post-content">
          <div class="user__post-title">Vue.js</div>
          <div class="user__post-desc">
            <span><b>JavaScript</b></span> framework for building interactive web applications ⚡
          </div>
          <div class="ratings__wrap">
            <div class="ratings__item">
              <iconMain class="starImg" name="starProfile" />
              <div class="starName">Star</div>
            </div>
            <div class="ratings__item">
              <div class="number__stars">156k</div>
            </div>
            <div class="ratings__item">
              <iconMain class="starImg" name="forkFile" />
              <div class="starName">Fork</div>
            </div>
            <div class="ratings__item">
              <div class="number__stars">4</div>
            </div>
          </div>
        </div>
      </template>
    </userProfile>
  </div>

</template>

<script>
import { topLine } from '../../components/topLine'
import { iconMain } from '../../icons'
import stories from './data.json'
import { storyUseritem } from '../../components/storyUserItem'
import { userProfile } from '../../components/userProfile'

export default {
  name: 'feedsPage',
  components: {
    topLine,
    iconMain,
    storyUseritem,
    userProfile
  },
  data () {
    return {
      stories
    }
  }
}
</script>
<style lang="scss" src="./feedsPages.scss" scoped>

</style>
