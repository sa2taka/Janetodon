<template>
  <div class="config-main">
    <b-tabs size="is-medium" v-model="activeTab" style="width: 100%;">
      <b-tab-item label="Accounts" icon="user-circle">
        <account-config></account-config>
      </b-tab-item>
      <b-tab-item label="Exclude Words" icon="filter">
        <exclude-words></exclude-words>
      </b-tab-item>
    </b-tabs>
  </div>
</template>

<script>
import AccountConfig from '@/components/Config/accounts'
import ExcludeWords from '@/components/Config/exclude_words'

export default {
  data () {
    return {
      activeTab: 0
    }
  },
  components: {
    AccountConfig,
    ExcludeWords
  },
  name: 'config-main'
}
</script>

<style lang="sass">
.config-main
  position: absolute
  display: flex
  border: solid 5px white
  border-radius: 40px
  background-color: $main-background
  width: 80vw
  height: 720px
  min-width: 500px
  top: 100px
  left: 64px
  padding: 10px

  &:after
    content: ""
    display: block
    position: absolute
    width: 0
    height: 0
    border-style: solid
    border-width: 0 10px 20px
    border-color: transparent transparent rgb(102, 96, 135)
    top: 48px
    left: -25px
    transform: rotate(-90deg)
</style>
