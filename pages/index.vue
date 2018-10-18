<template lang="pug">
  div.wrapper
    Header
    Banner(img="https://images.pexels.com/photos/265614/pexels-photo-265614.jpeg?w=1260&h=750&auto=compress&cs=tinysrgb", title="EDteam Styleguides", description="La presente guía de estilos define los componentes de diseño de EDteam y cómo implementarlos en nuestros productos.", :boton="true", :author="false")
    Main
      template(slot="main")
        p Esta guia define el concepto visual, patrones de diseño y estructura para proyectos web en EDteam.
        p Esta guia se encuentra en constante actualización.
        h2 Colores
        div.colors
          Color(cname="Principal", code="#007BDF", sassName="firstColor", cssName="first-color")
          Color(cname="Principal Alt", code="#006DC6", sassName="firstColorAlt", cssName="first-color-alt")

          Color(cname="Secundario", code="#00CBFF", sassName="secondColor", cssName="second-color")
          Color(cname="Secundario Alt", code="#006DC6", sassName="secondColorAlt", cssName="second-color-alt")

          Color(cname="Terciario", code="#FF3C32", sassName="thirdColor", cssName="third-color")
          Color(cname="Terciario Alt", code="#FF2419", sassName="thirdColorAlt", cssName="third-color-alt")

          Color(cname="Enfásis", code="#FBA905", sassName="accentColor", cssName="accent-color")
          Color(cname="Enfásis Alt", code="#F1A000", sassName="accentColorAlt", cssName="accent-color-alt")

          Color(cname="Oscuro", code="#282D31", sassName="darkColor", cssName="dark-color")
          Color(cname="Oscuro Alt", code="#141618", sassName="darkColorAlt", cssName="dark-color-alt")

          Color(cname="Bordes", code="#DFE0E0", sassName="borderColor", cssName="border-color")
          Color(cname="Texto", code="#53575A", sassName="textColor", cssName="text-color")
          Color(cname="Body BG", code="#FAFDFF", sassName="bodyBg", cssName="body-bg")

        h2 Tipografía
        p EDteam utiliza dos familias tipográficas en web, logotipo, posters y demás elementos gráficos
        ul.data-list
          li
            strong Open Sans (700)
            br
            span.small Encabezados, logo de EDteam y otros logos (EDgrid p.ej.)
              code $body-font
          li
            strong Lato (400, 400i, 700)
            br
            span.small Contenidos, párrafos
              code $heading-font
        p En la sección de <a href="tipografia.html">tipografía</a> se explica detalladamente su uso.
    footer.main-footer
      .ed-grid
        p.small EDteam Style Guide por&nbsp;
          a(href="http://alvarofelipe.net", target="_blank") Álvaro Felipe
</template>

<script>
import Color from '@/components/Color';
import Header from '@/components/Header';
import Banner from '@/components/Banner';
import Main from '@/components/Main';
import { mainBanner } from '@/helpers/utils';

export default {
  name: 'PageIndex',
  components: {
    Color,
    Main,
    Header,
    Banner
  },
  mounted() {
    mainBanner('.main-banner', '.main-header');
  }
};
</script>

<style lang="scss">
// Se agrega esta clase porque los estilos originales estan apuntado al body porque agrupa los elementos , en este caso el que agrupa es el div.wrapper
.wrapper {
  display: flex;
  flex-direction: column;
}
</style>
