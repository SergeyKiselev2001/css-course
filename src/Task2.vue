<template>
    <div class="container_2">
        <div class="banner">
            <h1 class="banner__heading">Subscribe here</h1>
            <div class="banner__arrow">
            </div>
            <button class="banner__btn">
                Click Now
            </button>
        </div>

        <div class="form-container">
            <form class="sign-up-form">
                <input type="text" class="form-input" placeholder="FULL NAME">
                <input type="email" class="form-input" placeholder="EMAIL ADDRES">
                <p>Get News?</p>
                <label>No</label>
                <input type="checkbox">
                <label>Yes</label>
                <button type="button">Sign Up Here</button>
            </form>

            <div class="form-container__header">
                <h1>Welcome to CodeAndCreate</h1>
            </div>

            <div class="x-btn">
                &#10005;
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'Task2.vue',
    components: {

    },

};


</script>

<style scoped>



@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:ital,wght@1,300&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto+Condensed:wght@700&display=swap');

.container_2{
    height: 100vh;
    width: 100%;

    background:linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.4)), url('../public/imgs/bgi-2nd.jpg') 0 0 no-repeat;
    background-size: cover;

    display: flex;
    justify-content: center;
    align-items: center;

    
}



.banner {
    display: none;

    color: white;
    width: 750px;
    
    flex-direction: column;
    align-items: center;
    justify-content: center;
    /* background-color: rgba(255, 0, 0, 0.212); */
    padding:10px;

}
.banner__arrow{
    background: url('../public/imgs/arrow.png') center / 40px 40px no-repeat;
    height: 70px;
    width: 50px;
    animation: anim 3s infinite;

}


.banner__heading{
    font-family: 'Roboto Condensed', sans-serif;
    font-size: 80px;
    margin-bottom: 60px;
    border-top: 7px solid white;
    border-bottom: 7px solid white;
}

.banner__btn{
    width: 200px;
    font-size: 18px;
    padding: 15px;
    font-family: 'Roboto Condensed', sans-serif;
    text-transform: uppercase;
    background-color: transparent;
    color: white;
    border: 3px solid white;
    cursor: pointer;
    letter-spacing: 2px;
    border-radius: 50px;
    outline: none;
    transition: .3s;
}

.banner__btn:hover{
    transform: translateY(-1px);
}

@keyframes anim {
    0%{
        transform: translateY(0);
    }
    20%{
        transform: translateY(0);
    }
    40%{
        transform: translateY(-30px);
    }
    50%{
        transform: translateY(0);
    }
    60%{
        transform: translateY(-15px);
    }
    80%{
        transform: translateY(0);
    }
    100%{
        transform: translateY(0);
    }
}

.form-container{
   background-color:rgba(255,0,0,0.2);
   width: 800px;
   height: 600px;
   position: absolute;
   box-shadow: 0 0 15px rgb(0, 0, 0);
   display: flex;
   
}

</style>