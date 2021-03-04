<template>
  <p>Reaction Time: {{ score }}ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if (this.score < 250) {
      this.rank = 'Faster than the Flash'
    } else if (this.score < 400) {
      this.rank = 'Cat like reflexes'
    } else {
      this.rank = `I didn't know snails could play this game...`
    }
  }
}
</script>

<style>

</style>