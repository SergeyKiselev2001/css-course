<template>
    <div class="container_5">
        <div class="banner">
            <div class="logo">
                <a href="#"><img src="../public/imgs/samurai.png" alt="logo"></a>
            </div>
            <div class="btn-wrapper">
                <button class="banner-btn">Explore More</button>
            </div>
        </div>

        <div class="nav-wrapper">
            <div class="hamburger-menu">
                <div class="line line-1"></div>
                <div class="line line-2"></div>
                <div class="line line-3"></div>
            </div>

            <nav class="top-nav" hidden>
                <ul class="nav-list">
                    <li>
                        <a href="#" class="nav-link">Home</a>
                    </li>
                    <li>
                        <a href="#" class="nav-link">About Us</a>
                    </li>
                    <li>
                        <a href="#" class="nav-link">Our Team</a>
                    </li>
                    <li>
                        <a href="#" class="nav-link">Services</a>
                    </li>
                    <li>
                        <a href="#" class="nav-link">Contact</a>
                    </li>
                </ul>
            </nav>


            <nav class="bottom-nav" hidden>
                <ul class="icons">
                    <li class="icon-item">
                        <a href="#" class="icon-link"><i class="fab fa-facebook-f"></i></a>
                    </li>
                    <li class="icon-item">
                        <a href="#" class="icon-link"><i class="fab fa-youtube"></i></a>
                    </li>
                    <li class="icon-item">
                        <a href="#" class="icon-link"><i class="fab fa-twitter"></i></a>
                    </li>
                    <li class="icon-item">
                        <a href="#" class="icon-link"><i class="fab fa-google-plus-g"></i></a>
                    </li>
                </ul>
            </nav>

        </div>
    </div>
</template>

<script>

export default {
    name: 'Task5.vue',
    components: {

    },

};


</script>

<style scoped>
@import url('../public/fontawesome-free-5.15.4-web/css/all.min.css');
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Slabo+27px&display=swap');

@font-face {
	font-family: 'Japanese-font'; 
	src: url('../public/HIROSHT.TTF'); 
}


*{
    color: white;
}
.fas {
    font-size: 50px;
}

.container_5{
    height: 100vh;
    width: 100%;

    background:linear-gradient(rgb(0, 0, 0), rgb(14, 35, 82));
    background-size: cover;

    display: flex;
    justify-content: center;
    align-items: center;

    font-family: 'Monsterrat', sans-serif;
}

.banner {
    width: 100%;
    height: 100vh;
    background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.2)), url('../public/imgs/japan.jpg') center no-repeat;
}

.logo {
    height: 160px;
    width: 180px;

    position: fixed;
    top:20px;
    left: 50px;
}


.logo img {
    width: 100%;
    height: auto;
    position: relative;
}



.hamburger-menu {
    width: 35px;
    height: 32px;
    
    position: fixed;
    top: 40px;
    right: 50px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    cursor: pointer;

}

.line {
    width: inherit;
    height: 5px;
    background-color: red;
    border-radius: 3px;
}


.btn-wrapper{
    position: absolute;
    top:50%;
    left:50%;
    transform: translate(-50%, -50%);
    perspective: 1000px;
}

.banner-btn{
    width: 350px;
    height: 100px;
    background: linear-gradient(rgb(199, 78, 41), rgb(139, 9, 9));
    outline: none;
    border: none;
    cursor: pointer;
    font-family: "Japanese-font", sans-serif;
    font-size: 28px;
    text-transform: uppercase;
    letter-spacing: 0px;


    text-shadow: 0 10px 10px black;

    transform: rotateX(70deg) rotateZ(40deg);
    transform-style: preserve-3d;

    transition: .5s;


    
}

.banner-btn:hover {
    transform: rotateX(20deg) rotateY(0deg);
    transition: linear-gradient transform .9s;
    background: linear-gradient(rgb(255, 138, 138), rgb(246, 184, 184));
    box-shadow: 0 10px 30px 10px rgb(255, 140, 140);

    text-shadow: 5px 10px 10px rgba(0, 0, 0, 0.253);
}

.banner-btn:hover::before{
     background: rgb(246, 184, 184);
}
.banner-btn:hover::after{
     background: rgb(246, 184, 184);
}



.banner-btn:active {
    box-shadow: 0 10px 30px 10px rgb(187, 139, 139);
 
    transform: translateY(15px);
}

.banner-btn:active::before{
     background: rgb(187, 139, 139);
 
}
.banner-btn:active::after{
     background: rgb(187, 139, 139);
     
}

.banner-btn::before{
    content: '';
    width: 100%;
    height: 25px;
    background: rgb(139, 9, 9);
    position: absolute;
    left: 0px;
    bottom: 0px;
    transform: rotateX(90deg);
    transform-origin: bottom;
}

.banner-btn::after{
    content: '';
    width: 25px;
    height: 100%;
    background: rgb(199, 78, 41);
    position: absolute;
    right: 0px;
    top: 0px;
    transform: rotateY(-90deg);
    transform-origin: right;
}

</style>