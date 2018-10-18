<template lang="pug">
  div.wrapper
    Header
    Banner(img="https://images.pexels.com/photos/265614/pexels-photo-265614.jpeg?w=1260&h=750&auto=compress&cs=tinysrgb", title="Tipografía", clase="tertiary")
    Main
      template(slot="main")
        p EDteam utiliza dos familias tipográficas:
        ul
          li
            strong Open Sans (700)
            |&nbsp;para los títulos
          li
            strong Lato (400,400i)
            |&nbsp;para los contenidos
        p Y los siguientes tamaños de fuente que se pueden conseguir con los elementos o clases indicados:
        ul.data-list
          li
            div
              div.biggest Biggest&nbsp;
                span.from-l (36px)
                span.to-l (24px)
            div
              p
                code &lt;h1&gt;&lt;/h1&gt;
                code .t1 .biggest
          li
            div
              div.bigger Bigger&nbsp;
                span.from-l (24px)
                span.to-l (20px)
            div
              p
                code &lt;h2&gt;&lt;/h2&gt;
                code .t2 .bigger
          li
            div
              div.big Big&nbsp;
                span.from-l (20px)
                span.to-l (16px)
            div
              p
                code &lt;h3&gt;&lt;/h3&gt;
                code .t3 .big
          li
            div
              div.normal Normal (16px)
            div
              p
                code &lt;h4&gt;&lt;/h4&gt;
                code .t4 .normal
          li
            div
              div.small Small (14px)
            div
              p
                code &lt;h5&gt;&lt;/h5&gt;
                code .t5 .small
          li
            div
              div.smaller Smaller (13px)
            div
              p
                code &lt;h6&gt;&lt;/h6&gt;
                code .t6 .smaller

        p Los títulos tienen&nbsp;
          code line-height: 1.3
          |&nbsp;y los contenidos&nbsp;
          code line-height: 1.6
          |. Las clases&nbsp;
          code .t1 .t2 .t3 .t4 .t5 .t6
          |&nbsp;aplican los tamaños de fuente indicados arriba con la tipografía y altura de línea para títulos. Las clases&nbsp;
          code .biggest .bigger .big .normal .small .smaller
          |&nbsp;aplican los tamaños de fuente indicados arriba con la tipografía de contenido. La clase &nbsp;
          code .normal
          |&nbsp;puede omitirse ya que representa el tamaño predeterminado. Salvo que se use para sobreescribir otro tamaño.

        h2 Aplicar tamaños de fuente sin clases (Sass)
        p Para los tres tamaños mayores use los mixins&nbsp;
          code t1
          code t2
          code t3
          |&nbsp;Para los tres tamaños menores use la funcion&nbsp;
          code fontSize($size)
          |&nbsp;donde el parámetro puede ser&nbsp;
          code normal | small | smaller
          |&nbsp;. La razon de separar los tamaños en dos grupos es que los más grandes (t1, t2, t3) se reducen en móviles para leerse mejor.

        h2 Blockquote
        blockquote El coronel destapó el tarro del café y comprobó que no había más de una cucharadita. Retiró la olla del fogón, vertió la mitad del agua en el piso de tierra, y con un cuchillo raspó el interior del tarro sobre la olla hasta cuando se desprendieron las últimas raspaduras del polvo de café revueltas con óxido de lata.

        h2 Enlaces
        p
          a(href="https://ed.team", target="_blank") EDteam
          |&nbsp; es la opción honesta y sin falsas promesas para aprender programación, diseño y emprendimiento en Latinoamerica y España. Visítanos en&nbsp;
          a(href="https://ed.team", target="_blank") ed.team
    footer.main-footer
      .ed-grid
        p.small EDteam Style Guide por &nbsp;
          a(href="http://alvarofelipe.net", target="_blank") Álvaro Felipe
</template>

<script>
import Banner from '@/components/Banner';
import Header from '@/components/Header';
import Main from '@/components/Main';
import { mainBanner } from '@/helpers/utils';

export default {
  name: 'PageTipografia',
  components: {
    Main,
    Banner,
    Header
  },
  mounted() {
    mainBanner('.main-banner', '.main-header');
  }
};
</script>

<style lang="scss" scoped>
// Se agrega esta clase porque los estilos originales estan apuntado al body porque agrupa los elementos , en este caso el que agrupa es el div.wrapper
.wrapper {
  display: flex;
  flex-direction: column;
}
</style>
