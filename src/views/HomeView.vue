<script setup lang="ts">
import { StreamBarcodeReader } from "vue-barcode-reader";
import { ImageBarcodeReader } from "vue-barcode-reader";
const onDecode =() =>{
    console.log('hi');
}
const onLoaded = ()=>{
  console.log('onLoad');
}
const onError = ()=>{
  console.log('on error ');
  
}
</script>

<template>
  <div>
    <ImageBarcodeReader @decode="onDecode" @error="onError"></ImageBarcodeReader>
    <StreamBarcodeReader @decode="onDecode" @loaded="onLoaded"></StreamBarcodeReader>
  </div>
</template>
