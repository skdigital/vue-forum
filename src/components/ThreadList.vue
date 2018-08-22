<template>
  <div>
    <h1>Welcome to the Forum</h1>
    <div class="thread-list">

      <h2 class="list-title">Threads</h2>

      <ThreadListItem
        v-for="thread in threads"
        :thread="thread"
        :key="thread['.key']"
      />
    </div>

    <div class="pagination">
      <button class="btn-circle" disabled><i class="fa fa-angle-left"></i></button>
      1 of 3
      <button class="btn-circle"><i class="fa fa-angle-right"></i></button>
    </div>
  </div>
</template>

<script>
  import ThreadListItem from './ThreadListItem'

  export default {
    components: {
      ThreadListItem
    },
    props: {
      threads: {
        required: true,
        type: Array
      }
    }
  }
</script>
