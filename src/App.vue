<template>
  <div style="text-align: center">
    <h1>LE CAPITALI EUROPEE</h1>
  </div>
  <table
    border="4"
    width="100%"
    style="position: absolute; top: 50% !important"
  >
    <tr>
      <td width="50%">
        ITALIA
        <rendered-box :propModel="italianFlag" />
      </td>
      <td width="50%">ROMA</td>
    </tr>
    <tr>
      <td width="50%">
        FRANCIA
        <rendered-box :propModel="frenchFlag" />
      </td>
      <td width="50%">PARIGI</td>
    </tr>
    <tr>
      <td width="50%">
        GERMANIA
        <rendered-box :propModel="germanFlag" />
      </td>
      <td width="50%">BERLINO</td>
    </tr>
    <tr>
      <td width="50%">
        GRAN BRETAGNA
        <rendered-box :propModel="britainFlag" />
      </td>
      <td width="50%">LONDRA</td>
    </tr>
    <tr>
      <td width="50%">
        SPAGNA
        <rendered-box :propModel="spainFlag" />
      </td>
      <td width="50%">MADRID</td>
    </tr>
  </table>
</template>
<script>
import RenderedBox from "./components/RenderedBox.vue";
const frenchFlagUrl = new URL ('./models/frenchFlag.gltf',import.meta.url).href
const germanFlagUrl = new URL ('./models/germanFlag.gltf?raw',import.meta.url).href
const italianFlagUrl= new URL ('./models/italianFlag.gltf?raw',import.meta.url).href
const britainFlagUrl= new URL('./models/britainFlag.gltf?raw',import.meta.url).href
const spainFlagUrl= new URL ('./models/spainFlag.gltf?raw',import.meta.url).href

export default {
  data() {
    return {
      frenchFlag: frenchFlagUrl,
      italianFlag: italianFlagUrl,
      germanFlag: germanFlagUrl, 
      britainFlag: britainFlagUrl, 
      spainFlag: spainFlagUrl 
    };
  },
  components: {
    RenderedBox,
  },
};
</script>

<style>
</style>
