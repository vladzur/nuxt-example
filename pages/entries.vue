<template>
  <div class="container">
    <simple-card title="New entry">
      <vz-input type="text" v-model="entry.title" placeholder="Title"></vz-input>
      <vz-input type="text" v-model="entry.text" placeholder="Text"></vz-input>
    </simple-card>
    <hr></hr>
    <simple-card :title="entry.title">
      {{ entry.text}}
    </simple-card>
  </div>
</template>

<script>
import SimpleCard from '~components/SimpleCard'
import VzInput from '~components/VzInput'
export default {
  components: { SimpleCard, VzInput },
  data () {
    return {
      entry: {
        title: '',
        text: ''
      }
    }
  }
}
</script>

<style>

</style>
