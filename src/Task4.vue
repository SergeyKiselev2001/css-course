<template>
    <div class="container_4">
        
        <div v-if="banner" class="banner">
            <h1>Code And Create</h1>
            <button v-on:click="banner = !banner" type="button">Start Slideshow</button>
        </div>

        <div v-if="!banner" class="slideshow-wrapper">
            <div class="slideshow">
                <div class="slide">
                    <div class="content">
                        <h3>London</h3>
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minus sapiente libero ipsum magnam voluptatum amet, ipsam vero architecto repellendus neque fugiat repellat quam nihil aliquid recusandae id nisi! Molestias, quaerat.</p>
                        <button type="button">Read More <i class="arrow"></i></button>
                    </div>
                </div>

                <div class="slide">
                    <div class="content">
                        <h3>New York</h3>
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minus sapiente libero ipsum magnam voluptatum amet, ipsam vero architecto repellendus neque fugiat repellat quam nihil aliquid recusandae id nisi! Molestias, quaerat.</p>
                        <button type="button">Read More <i class="arrow"></i></button>
                    </div>
                </div>

                <div class="slide">
                    <div class="content">
                        <h3>Tokyo</h3>
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minus sapiente libero ipsum magnam voluptatum amet, ipsam vero architecto repellendus neque fugiat repellat quam nihil aliquid recusandae id nisi! Molestias, quaerat.</p>
                        <button type="button">Read More <i class="arrow"></i></button>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script>

export default {
    name: 'Task4.vue',
    components: {

    },

    data(){
        return {
            banner: true,
        }
    }

};


</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Montserrat:wght@200&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Dosis:wght@500&display=swap');

*{
    color: white;
}


.container_4{
    height: 100vh;
    width: 100%;

    /* background:linear-gradient(rgb(0, 0, 0), rgb(0, 0, 0)); */
    background-size: cover;

    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0px;
    margin: 0px;

}

.banner {
    text-align: center;

    background: linear-gradient(100deg, rgba(255, 10, 243, 0.1) 10%, rgb(0, 0, 0, 0) 90%);
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

}

.banner h1{
    font-family: 'Josefin Sans', sans-serif;
    font-weight: 900;
    font-size: 60px;
    color: rgb(170, 80, 255);
  
    position: relative;

    border-bottom: 3px solid rgb(170, 80, 255);
    padding: 5px;
    padding-top: 10px;
    letter-spacing: 3px;

    ;

}

.banner h1::after {
    content: "";
    height: 110%;
    width: 200%;

    left: -200px;
    top: -2px;
    /* border: 1px solid red;  */
    position: absolute;
    animation-name: banner-h1;
    animation-duration: 3s;
    animation-delay: .5s;
    animation-fill-mode: forwards;
    animation-iteration-count: 1;
    transition: 1s;
    animation-timing-function: ease;
    overflow: hidden;
    background: linear-gradient(90deg, rgba(0,0,0,.01) 0%, rgba(0,0,0,1) 20%);
}

@keyframes banner-h1 {
    0%{
       left: -200px;
    }
    100%{
        left: 480px;
         
    }
}

.banner button {
    margin-top: 40px;
    padding: 15px 50px;
    color: rgb(255, 255, 255);
    font-size: 26px;
    cursor: pointer;
    background: linear-gradient(90deg, rgb(170, 80, 255), rgb(145, 70, 216));
    font-family: 'Josefin Sans', sans-serif;
   
    border-radius: 40px;
    font-weight: 100;
    transition: .4s;
    outline: none;
    
    transform: perspective(500px) rotateY(-15deg);
    text-shadow: 6px 3px 2px rgba(0,0,0,0.4);
    overflow: hidden;
}



.banner button:hover {
    transform: perspective(500px) rotateY(0deg);
    text-shadow: -1px 3px 2px rgba(0,0,0,0.4);
    background: linear-gradient(90deg, rgb(145, 70, 216), rgb(118, 38, 192));
}


.banner button::after{
    content: '';
    height: 100%;
    width: 100%;
    position: absolute;
    left: -240px;
    top: 0px;
    background: linear-gradient(to right, transparent, rgba(255,255,255,.8), transparent);
    /* border: 1px solid red; */
    transition: .6s;
}

.banner button:hover::after{
   left: 300px; 
}

.slideshow-wrapper {
   position: relative;
   height: 100vh;
   width: 100%;
   opacity: 0;
   animation: poyavlenie 1s 1 forwards;

}

@keyframes poyavlenie {
    from {
        opacity: 0;
    }

    to {
        opacity: 1;
    }
}

.slideshow {
    display: flex;
    flex-direction: row;
    width: 300%;
    position: relative;
    animation: slideshow 20s infinite;
}

@keyframes slideshow {
    0%{ left: 0; }
    12%{ left: 0; }
    20%{ left: -100%; }
    42%{ left: -100%;}
    50%{ left: -200%;}
    62%{ left: -200%;}
    72%{ left: -100%; }
    80%{ left: -100%;}
    92%{ left: 0; }
    100%{ left: 0; }
}


.slide {
    width: 100%;
    margin:0px;
    height: 100vh;
    

}

.slide:nth-child(1){
    background: linear-gradient(40deg, rgba(0,0,0,0.6) 30%, rgba(0,0,0,0.1)), url('../public/imgs/london.jpg') center no-repeat;
    background-size: cover;
}

.slide:nth-child(2){
    background: linear-gradient(40deg, rgba(0,0,0,0.6) 30%, rgba(0,0,0,0.1)), url('../public/imgs/nyc.png') center no-repeat;
    background-size: cover;
}

.slide:nth-child(3){
    background: linear-gradient(40deg, rgba(0,0,0,0.6) 30%, rgba(0,0,0,0.1)), url('../public/imgs/tokyo.jpg')center no-repeat;
    background-size: cover;
}

.slide {
    padding-top: 200px;
}

.content {
    width: 530px;
    margin-left: 10%;
    
}

.content h3 {
    font-size: 64px;
    letter-spacing: 2px;
    font-family: 'Dosis', sans-serif;
    
}

.content p {
    font-size: 24px;
    font-family: 'Montserrat', sans-serif;
    line-height: 32px;
    margin-top: 30px;
}

.content button {
    
    padding: 10px 30px;
    background: transparent;
    
    outline: none;
    border: 1px solid white;
    border-radius: 25px;
    font-size: 20px;
    font-family: 'Montserrat', sans-serif;
    margin-top: 20px;
    transition: .2s;
    cursor: pointer;
}

.content button:hover{
    background: white;
    color: black;
}

.content button:active{
    border: 1px solid rgb(98, 98, 98);
    background: rgb(98, 98, 98);
    color: black;
}


</style>