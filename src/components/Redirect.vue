<page-query>
query Redirect ($id: ID!) {
   blog (id: $id) {
    path
  }
}
</page-query>

<script>
export default {
  metaInfo() {
    return {
        title: `Site has moved to ${this.$page.blog.path}`,
        meta: [
            { 'http-equiv': 'refresh', content: `0; URL=${this.$page.blog.path}`}
        ],
    }
  }
}
</script>

