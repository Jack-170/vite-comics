<script>
import HeaderComics from './components/HeaderComics.vue';
import ContentSection from './components/ContentSection.vue';
import IconsSection from './components/IconsSection.vue';




export default{
    components:{
      HeaderComics,
      ContentSection,
      IconsSection
    }
}

</script>

<template>

 <HeaderComics />

 <main>

  <ContentSection/>

  <IconsSection/>
  
 </main>
 
</template>

<style lang="scss">
@use './styles/general.scss' as *;

</style>
