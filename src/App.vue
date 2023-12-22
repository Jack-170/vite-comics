<script>
import HeaderComics from './components/HeaderComics.vue';
import ContentSection from './components/ContentSection.vue';
import IconsSection from './components/IconsSection.vue';
import ListSection from './components/ListSection.vue';




export default{
    components:{
      HeaderComics,
      ContentSection,
      IconsSection,
      ListSection
    }
}

</script>

<template>

 <HeaderComics />

 <main>

  <ContentSection/>

  <IconsSection/>

  <ListSection/>
  
 </main>
 
</template>

<style lang="scss">
@use './styles/general.scss' as *;

</style>
