<template>
  <div class="col-full">
    <ThreadList :threads="threads"/>
  </div>
</template>

<script>
  import ThreadList from '@/components/ThreadList'
  import sourceData from '@/data'

  console.log(sourceData)

  export default {
    components: {
      ThreadList
    },
    data () {
      return {
        threads: Object.values(sourceData.threads),
        posts: sourceData.posts,
        users: sourceData.users
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
