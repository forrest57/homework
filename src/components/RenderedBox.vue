<template>
  <Renderer
    ref="renderer"
    antialias
    :orbit-ctrl="{ enableDamping: true }"
    resize="window"
  >
    <Camera :position="{ z: 50 }" />
    <Scene background="#ffffff">
      <PointLight :position="{ x: 100, y: 50, z: 50 }" />
      <PointLight :position="{ x: 100, y: 0, z: 0 }" />
      <PointLight :position="{ x: 100, y: 100, z: 100 }" />
      <!-- <Box ref="box" :rotation="{ y: Math.PI / 4, z: Math.PI / 4 }"> -->

      <!-- <LambertMaterial /> -->
      <!-- </Box> -->
      <!-- <AmbientLight></AmbientLight> -->
      <GltfModel
        :src="propModel"
        :rotation="{ y: Math.PI / 4, z: Math.PI / 4 }"
        ref="model"
      />
    </Scene>
  </Renderer>
</template>

<script>
export default {
  name: "RenderedBox",
  props: {
    propModel: String,
  },
  async mounted() {
    // setTimeout(() => {
    // await resolve(this.propModel);
    console.log(this.propModel);
    const renderer = await this.$refs.renderer;
    console.log(this.$refs.box);
    const model = await this.$refs.model.scene;
    renderer.onBeforeRender(() => {
      model.rotation.x += 0.01;
    });
    // }, 2000);
  },
};
</script>

<style>
body {
  margin: 0;
}
canvas {
  height: 100%;
  width: 100%;
  display: block;
}
</style>
