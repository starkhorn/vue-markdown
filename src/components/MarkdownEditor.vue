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
          <textarea cols="100" rows="20" v-model="content">
              </textarea>
        </td>
        <td>
          <div v-html="renderedContent"></div>
        </td>
      </tr>
    </tbody>
  </table>
</div>
</template>

<script>
import MarkdownIt from 'markdown-it'

const md = new MarkdownIt({
  breaks: true
})

export default {

  data() {
    return {
      content: ''
    }
  },

  computed: {
    renderedContent() {
      return md.render(this.content)
    }
  }
}
</script>
