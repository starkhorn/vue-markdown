<style scope>
  #editor td {
    vertical-align: top;
  }
</style>

<template>
  <div id="app">
    <h1>Markdown Editor</h1>

    <MarkdownEditor></MarkdownEditor>
  </div>
</template>

<script>
  import MarkdownEditor from './components/MarkdownEditor'

  export default {

    components: {
      MarkdownEditor
    }
  }
</script>
