<template lang="pug">

.curso-main-container.pb-3
  
  .container.tarjeta.tarjeta--blanca 
    SlyderB.mb-5(:datos="datosSlyder")

    .curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
  
    .titulo-principal
      .titulo-principal__numero
        span
          i.fas.fa-info
      h1 Introducción
    
    figure.mb-5
      .video
        iframe(width="560" height="315" src="https://www.youtube.com/embed/2L91WMqw96A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)
      figcaption Video: Leyenda del video



            
</template>

<script>
export default {
  components: {},
  data: () => ({
    datosSlyder: [
      {
        titulo: 'Tabaco que se quema',
        texto:
          'Los cigarrillos combustibles, puros, cigarritos y pipas están hechos de hojas de tabaco y aditivos. El humo de tabaco generado por la combustión del tabaco contiene miles de sustancias químicas, pero al menos 70 de estas son agentes cancerígenos. La nicotina es el ingrediente que produce la adicción en las personas (American Cancer Society, 2019).',
        imagen: require('@/assets/template/Introduccion/Tabacosequema.png'),
        // leyendaImagen: 'Leyenda de la imagen',
      },
      {
        titulo: 'Tabaco sin humo',
        texto:
          'Son productos que no se queman, incluye el tabaco en polvo o rapé (rapé seco o húmedo), el tabaco soluble y el tabaco para masticar. Estos productos contienen sustancias carcinógenas como las nitrosaminas, el benzopireno y otros hidrocarburos aromáticos policíclicos. Al igual que otras formas de tabaco contiene sustancias radiactivas y nicotina. Su consumo aumenta el riesgo de padecer neoplasias de cabeza y cuello y cáncer de boca (American Cancer Society, 2019).',
        imagen: require('@/assets/template/Introduccion/sinhumo.png'),
        // leyendaImagen: 'Leyenda de la imagen',
      },
      {
        titulo: 'Productos de tabaco solubles',
        texto:
          'Son productos con formas específicas redondeadas o alargadas, muy similares en su forma a los dulces comestibles.',
        imagen: require('@/assets/template/Introduccion/tabaco.png'),
        // leyendaImagen: 'Leyenda de la imagen',
      },
    ],
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>
