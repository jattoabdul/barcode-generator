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
        <h3>Bar Code</h3>
        <barcode :value="barcodeValue">
          No Barcode generated
        </barcode>
      </div>
      <div class="qrcode-img-container">
        <h3>QR Code</h3>
        <qrcode :value="barcodeValue" level="H" />
      </div>
    </div>
  </div>
</template>

<script>
import VueBarcode from 'vue-barcode'
import QrcodeVue from 'qrcode.vue'

export default {
  components: {
    'barcode': VueBarcode,
    'qrcode': QrcodeVue
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
