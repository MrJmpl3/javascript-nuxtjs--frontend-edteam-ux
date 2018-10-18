<template lang="pug">
  v-fragment
    #vertical-menu-toggle.vertical-menu-toggle.to-l(data-content="Filtros")
    nav.vertical-menu#vertical-menu
      ul
        li
          nuxt-link(to="/") Inicio
        li
          nuxt-link(to="/tipografia") Tipografia
        li: a(href="/botones.html") Botones
        li: a(href="/tablas.html") Tablas
        li: a(href="/listas.html") Listas
        li: a(href="/formularios.html") Formularios
        li: a(href="/cards.html") Cards
        li: a(href="/post.html") Post
        li: a(href="/banner.html") Banner
        li: a(href="/topbar.html") Top bar
        li: a(href="/modal.html") Modal
        li: a(href="/tabs.html") Tabs
        li: a(href="/iconos.html") Iconos
        li: a(href="/playlist.html") Playlist
        li: a(href="/pricing-table.html") Tabla de precios
        //li: a(href="/video-class.html") Video
        //li: a(href="/video-live.html") Live
        //li: a(href="/curso.html") Curso
</template>

<script>
export default {
  name: 'TopicMenu',
  components: {}
};
</script>

<style scoped>
</style>
