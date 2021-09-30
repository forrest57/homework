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
export default {
  data() {
    return {
      frenchFlag: "src/models/frenchFlag.gltf",
      italianFlag: "src/models/italianFlag.gltf",
      germanFlag: "src/models/germanFlag.gltf",
      britainFlag: "src/models/britainFlag.gltf",
      spainFlag: "src/models/spainFlag.gltf",
    };
  },
  components: {
    RenderedBox,
  },
};
</script>

<style>
</style>
