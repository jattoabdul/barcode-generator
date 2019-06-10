<template>
  <div class="container">
    <div>
      <h1 class="title">
        Barcode Generator
      </h1>
      <h2 class="subtitle">
        Enter a text below and click on generate to generate a barcode
      </h2>
      <div class="text-input">
        <input v-model.trim="barcodeValue" type="text">
      </div>
      <!-- <button>
        Generate Barcode
      </button> -->
      <div class="barcode-img-container">
        <barcode :value="barcodeValue">
          No barcode generated
        </barcode>
      </div>
    </div>
  </div>
</template>

<script>
import VueBarcode from 'vue-barcode'

export default {
  components: {
    'barcode': VueBarcode
  },
  data() {
    return {
      barcodeValue: ''
    }
  },
  methods: {
    // generateBarCode() {
    //   console.log('====>', this.codeText)
    // }
  }
}
</script>

<style lang="scss" src="./index.scss" scoped />
