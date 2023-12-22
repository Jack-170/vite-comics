<script>
export default{
    name:"ContentSection",
    
 }

</script>

<template>

    <div class="list-section">
        <div class="container">

            <div>

                <ul>
                    <li>
                        <h3>Dc Comics</h3>
                    </li>

                    <li>Characters</li>

                    <li>Comics</li>

                    <li>Movies</li>

                    <li>TV</li>

                    <li>Games</li>

                    <li>Videos</li>

                    <li>News</li>

                    <li>
                        <h3>Shop</h3>
                    </li>

                    <li>Shop DC</li>

                    <li>Shop DC Collectibles</li>
                
                </ul>


            </div>


            <div>
                <ul>
                    <li>
                        <h3>Dc</h3>
                    </li>

                    <li>Terms of use </li>

                    <li>Privacy policy(new)</li>

                    <li>Ad Choiches</li>

                    <li>Advertising</li>

                    <li>Jobs</li>

                    <li>Subscriptions</li>

                    <li>Talent Workshops</li>


                    <li>Cpsc Certificates</li>

                    <li>Ratings</li>

                    <li>Shop help</li>
                    <li>COntact us</li>
                </ul>


            </div>

            <div>
                <ul>
                    <li>
                        <h3>Sites</h3>
                    </li>

                    <li>DC</li>

                    <li>Mad Magazine</li>

                    <li>DC Kids</li>

                    <li>DC Universe</li>

                    <li>DC Power Visa</li>

                    
                </ul>


            </div>
            
        </div>
    </div>

    
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/mixins' as *;




.list-section{
    width: 100%;
    background-image: url("../assets/images/footer-bg.jpg" );

    .container{
        display: flex;
        color: white;
        padding: 1.5rem;

    }
   
}


ul{
    padding: 1rem;
    list-style-type: none;


    li{
        font-size: 14px;
        color: #6b655d;
    }

    li h3{
        margin: 10px 0;
        color: white;
        font-size: 19px;
    }
}




</style>
