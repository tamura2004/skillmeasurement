<template lang="pug">
.container
  .card.card-block(
    v-for="user in users",
    @click="LIST_USER_SKILLS(user.id)"
  )
    h5.card-title {{ user.name }}
    p 回答：{{ user.skillNum }}/123

</template>

<script>
import { LIST_USER_SKILLS } from '../vuex/mutation-types'
import { mapGetters, mapActions } from 'vuex'

export default {
  name: 'hello',
  methods: mapActions([LIST_USER_SKILLS]),
  computed: mapGetters(['users', 'userSkills'])
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.card
  width: 12rem
  display inline-block
  margin 1rem 2rem
  text-align center
</style>
