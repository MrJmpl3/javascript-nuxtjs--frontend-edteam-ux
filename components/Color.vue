<template lang="pug">
  .color
    div(:class="`color__sample ${sassName}`")
    .color__info.smaller
      p.color__name {{ cname }}
      p.color__code {{ code }}
      p.color__code Sass name:
        code {{ `$${sassName}` }}
      p.color__code CSS name:
        code {{ `--${cssName}` }}
</template>

<script>
export default {
  name: 'Color',
  props: {
    cname: {
      required: true,
      type: String
    },
    code: {
      required: true,
      type: String
    },
    sassName: {
      required: true,
      type: String
    },
    cssName: {
      required: true,
      type: String
    }
  }
};
</script>

<style scoped>
</style>
