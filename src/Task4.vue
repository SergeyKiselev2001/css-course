<template>
    <div class="container_4">
        
        <div class="banner">
            <h1>Code And Create</h1>
            <button type="button">Start Slideshow</button>
        </div>

        <div class="slideshow-wrapper">
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
                        <h3>LNew York</h3>
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

};


</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans&display=swap');

*{
    color: white;
}


.container_4{
    height: 100vh;
    width: 100%;

    background:linear-gradient(rgb(0, 0, 0), rgb(0, 0, 0));
    background-size: cover;

    display: flex;
    justify-content: center;
    align-items: center;

    
}

.banner {
    text-align: center;
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
}



button:hover {
    transform: perspective(500px) rotateY(0deg);
    text-shadow: -1px 3px 2px rgba(0,0,0,0.4);
    background: linear-gradient(90deg, rgb(145, 70, 216), rgb(118, 38, 192));
}


.slideshow-wrapper {
    display: none;
}


</style>