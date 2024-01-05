<script>
export default{
    name:"HeaderComics",

    props:{
        links:Array,
    }

}
</script>

<template>

    <header>
        
        <div class="container">

            <a href="" class="box-img">
                <img src="../assets/images/dc-logo.png" alt="">
            </a>

           <ul>
                <li v-for="link in links">
                    <a :href="link.url" :class="link.current ? 'active':''">{{link.text}}</a>
                </li>  
           </ul>
  

        </div>
        



    </header>

    
  
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/mixins' as *;

.container{
    @include space-between;
    font-size: 14px;

    .box-img{
        height: 70px;
        width: 70px;
    }

    ul{
        list-style-type:none;
        display: flex;

        li a{
            text-decoration: none;
            padding: 1rem;
            color: black;

            &.active,
            &:hover {
                color: #4fadf9; 
                
                border-bottom: 3px solid #4fadf9;
                
            }
        }

    }
}

header{
    height: 100px;
    background-color: white;
}



</style>
