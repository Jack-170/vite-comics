<script>
export default{
    name:"ContentSection",
    
 }

</script>

<template>

    <div class="content-section">
        <div class="container">

            <h3> {{ '--->' }}Content goes here{{ '<---' }}  </h3>

        </div>
    </div>
    
    
  
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/mixins' as *;

.content-section{
    width: 100%;
    height: 100px;
    background-color: #1c1c1c;

    .container{
        @include align-center;
        h3{
            color: white;
        }
    }

}










</style>
