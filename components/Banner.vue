<template lang="pug">
  div(:class="`main-banner--${clase} main-banner`")
    div.ed-container
      div.ed-item.l-75.to-center
        img.main-banner__img(:src="img")
        div.main-banner__data
          h1 {{ title }}
          slot(v-if="description !== ''")
            p.subtitle {{ description }}
          slot(v-if="boton")
            a.button--cta.small.center(href="#") Modelo de botón
          slot(v-if="author")
            .main-banner__author
              a(href="#")
                img.main-banner__author-img(src="https://ed.team/sites/default/files/styles/thumbnail/public/pictures/2017-11/alexys_0.jpg?itok=MMRiEdrl")
              a(href="#")
                div.main-banner__author-name Alexys Lozada
</template>

<script>
export default {
  name: 'Banner',
  props: {
    img: {
      required: true,
      type: String
    },
    title: {
      required: true,
      type: String
    },
    description: {
      default: '',
      type: String
    },
    clase: {
      default: '',
      type: String
    },
    boton: {
      default: false,
      type: Boolean
    },
    author: {
      default: false,
      type: Boolean
    }
  }
};
</script>

<style scoped>
</style>
