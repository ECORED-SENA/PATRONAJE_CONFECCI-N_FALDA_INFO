<template lang="pug">
section
  BannerPrincipal.mb-5


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 1. Presentación

    p Estimado aprendiz, bienvenido a este nuevo reto de su vida académica en la que se busca una competencia relacionada con la confección de falda como lo verá en el siguiente video; recuerde que en el SENA se forman colombianos para el fomento de la industria.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 2. Justificación<br>del programa

    p El sector de la confección en la actualidad es uno de los más dinámicos de la economía colombiana, generando 70% del empleo y 6% del producto interno bruto (ProColombia, s.f., Colombia Productiva, s.f.).
      br
      br
      |A pesar de que el sector tiene una alta proyección económica se han detectado necesidades de nuevos puestos de trabajo y actualización del talento humano como lo muestra el informe de Identificación y cierre de brechas de capital humano para el clúster de prendas de vestir de Bogotá-región, realizado por la CCB y el Programa de la Naciones Unidas para el Desarrollo (PNUD) que, además, evidencia la necesidad de consolidar al sector de la confección como de clase mundial, resaltando la competitividad, el fortalecimiento empresarial, crecimiento de la industria, acceso a nuevos mercados y la garantía de la multiplicación de ingresos del sector.
      br
      br
      |Como política del Gobierno mediante el Programa de Colombia Productiva, en donde intervienen las instituciones públicas y privadas, se trabaja con el propósito de ofrecer programas de formación para cualificar el talento humano en el campo laboral de la confección. 
      br
      br
      |En este marco el SENA ofrece el programa Patronaje y confección industrial de falda, con un componente técnico, basado en normas de competencia laboral, en donde se integran habilidades cognitivas como el análisis de materias primas, insumos, herramientas, interpretación de diseño, guía operacional y el desarrollo de habilidades motrices en manipulación de materiales que beneficiarán al aprendiz en su inmersión en el campo laboral o en el desarrollo de su propio emprendimiento.


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Población<br>objetivo

    p 
      b 290601224 - 
      b-none Confeccionar prendas sobre medida según técnicas de sastrería y modistería.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 4. Estrategia<br>metodológica

    p entrada en la construcción de autonomía para garantizar la calidad de la formación en el marco de la formación por competencias, el aprendizaje por proyectos y el uso de técnicas didácticas activas que estimulan el pensamiento para la resolución de problemas simulados y reales; soportadas en la utilización de las tecnologías de la información y la comunicación, integradas en ambientes virtuales de aprendizaje que, en todo caso, recrean el contexto productivo y vinculan al aprendiz con la realidad cotidiana y el desarrollo de las competencias. 
      br
      br
      |Igualmente, debe estimular de manera permanente la autocrítica y la reflexión del aprendiz sobre el quehacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento:
    ul.lista-ul
        li 
          i.lista-ul__vineta
          | El instructor – tutor.
        li 
          i.lista-ul__vineta
          | El entorno.
        li 
          i.lista-ul__vineta
          | Las TIC.
        li 
          i.lista-ul__vineta
          | El trabajo colaborativo.



  //- Créditos
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 Créditos

    CreditosComp

  Footer
  

</template>
<script>
import { menuPrincipal } from '../config/global'
import BannerPrincipal from '../components/plantilla/BannerPrincipal'
import CreditosComp from '../components/plantilla/CreditosComp'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Inicio',
  components: {
    BannerPrincipal,
    CreditosComp,
    Footer,
  },
  data: () => ({
    menuPrincipalData: menuPrincipal,
  }),
  computed: {
    desarrolloContenidosData() {
      const allMenuData = [
        ...this.menuPrincipalData.menu,
        ...this.menuPrincipalData.subMenu,
      ]
      return allMenuData.filter(item => item.desarrolloContenidos)
    },
  },
}
</script>

<style lang="sass" scoped>
.resultados-aprendizaje
  &__item
    margin-bottom: 20px
    &:last-child
      margin-bottom: 0

.desarrollo-contenidos
  &__item
    display: flex
    align-items: center
    justify-content: space-between
    margin-bottom: 25px
    padding: 5px
    border-radius: $base-border-radius

    &__texto
      display: flex
      align-items: center

    &__icono
      display: block
      background-color: $color-sistema-g
      font-size: 20px
      font-weight: $base-black-font-weight
      text-align: center
      padding: 10px
      line-height: 1em
      width: 40px
      margin-right: 15px

    &:last-child
      margin-bottom: 0

    &:hover
      background-color: $color-sistema-g
      font-weight: $base-black-font-weight
      color: $color-sistema-a
</style>
