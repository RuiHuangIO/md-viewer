<template>
  <div class="container">
    <div class="row center">
      <h2>Vue Markdown Viewer</h2>
    </div>
    <div class="row">
      <div class="col s12 m6 l6 xl6">
        <div class="center">
          <h4>Markdown</h4>
          <textarea v-model="markdown" class="info"></textarea>
        </div>
      </div>

      <div class="col s12 m6 l6 xl6">
        <div>
          <h4 class="center">Preview</h4>
          <div :key="markdown" class="info" v-markdown>{{markdown}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data(){
    return{
      markdown: '',
    };
  },
};
</script>

<style scoped>
textarea {
  resize: none;
  border: 2px dashed orange;
  outline: none;
}

.info {
  height: 400px;
  width: 100%;
  background-color: rgba(255, 255, 255, 0.9);
}
</style>
