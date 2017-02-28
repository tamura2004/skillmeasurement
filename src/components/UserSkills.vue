<template lang="pug">
.container
  h3 username: {{ user.name }}
  h4(v-for="proc in skilltree.procs") proces: {{ proc.name }}
    h5(v-for="act in proc.acts") activity: {{ act.name }}
      h5(v-for="skill in act.skills") skill: {{ skill.name }}
        form
          div(v-for="i in 5") {{ i}}
            label.radio-inline {{ i}}
            input(type="radio",@change="alert(i)")

</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'hello',
  computed: mapGetters(['user', 'skilltree', 'userSkills'])
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.card
  width: 12rem
  display inline-block
  margin 1rem 2rem
  text-align center

h4, h5, label
  margin-left 2rem
  
</style>
