<template>
  <div id="app">
    <h1>bla</h1>
  </div>
</template>

<script>
import Unicrypto from 'unicrypto'

export default {
  name: 'App',
  created () {
    this.initUnicrypto()
  },
  methods: {
    async initUnicrypto () {
      const options = { strength: 2048 }
      const priv = await Unicrypto.PrivateKey.generate(options)
      console.log(priv)
    }
  },
}
</script>
