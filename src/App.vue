<template>
  <div id="app">
    <h1>Modal example</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos ullam id fuga, rerum laborum quibusdam inventore, nemo in velit voluptatibus ipsum quis dolorem ab nulla. Dignissimos nam reiciendis animi dolor.
    </p>
    <button href="#" @click.prevent="$refs.welcome.open()">Open Welcome Modal</button>
    <button href="#" @click.prevent="$refs.other.open()">Open Other Modal</button>

    <modal ref="welcome">
      <h2>Welcome</h2>
    </modal>

    <modal ref="other">
      <h2>Other Modal</h2>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. In, nobis voluptatem? Beatae esse mollitia veniam modi fugiat accusamus, exercitationem animi odio consequuntur id iure quae ad nisi quidem, suscipit nesciunt?
      </p>
    </modal>

  </div>
</template>

<script>
import Modal from './components/modal.vue'
export default {
  name: 'app',
  components: {
    Modal
  },
  mounted() {
    console.log(this.$refs.loginModal);
  }
}
</script>

<style lang="scss">

</style>
