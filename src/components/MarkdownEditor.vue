<style scope>
  #editor td {
    vertical-align: top;
  }
</style>

<template>
  <div>
    <table id="editor">
      <tbody>
        <tr>
          <td>
            <textarea cols="100" rows="20" v-model="rawContent">
            </textarea>
          </td>
          <td>
            <div v-html="renderedContent"></div>
          </td>
        </tr>
      </tbody>
    </table>

    <button @click="preview">Preview</button>
  </div>
</template>

<script>
  export default {

    data () {
      return {
        rawContent: '',
        renderedContent: ''
      }
    },

    methods: {
      preview () {
        // TODO: transform raw content to rendered
        this.renderedContent = this.rawContent
      }
    }
  }
</script>