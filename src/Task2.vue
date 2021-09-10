<template>
    <div class="container_2">
        <div v-if='current_page==1' class="banner">
            <h1 class="banner__heading">Subscribe here</h1>
            <div class="banner__arrow">
            </div>
            <button 
                @click=" this.current_page=2"
                class="banner__btn">
                Click Now
            </button>
        </div>

        <div v-if='current_page==2' class="form-container">
            <form class="form-container__sign-up-form">
                <input type="text" class="form-input" placeholder="FULL NAME">
                <input type="email" class="form-input" placeholder="EMAIL ADDRES">
                <p>Get News?</p>
                <label>No</label>
                <input type="checkbox">
                <label>Yes</label>
                <div class="button-wrapper">
                    <div class='sign-up-button'>Sign Up Here</div>
                    <div class="sign-over"></div>
                </div>
                
            </form>

            <div class="form-container__header">
                <h1>Welcome to CodeAndCreate</h1>
                <div class="under-anim"></div>
            </div>

            <div 
                @click="current_page=1"
                class="x-btn">
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

    data(){
        return {
            current_page : 1
        }
    }

};


</script>

<style scoped>



@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:ital,wght@1,300&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto+Condensed:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200&display=swap');


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
    display: flex;

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
    opacity: 0;
   background-color:rgba(255,0,0,0.2);
   width: 800px;
   height: 600px;
   position: absolute;
   box-shadow: 0 0 15px rgb(0, 0, 0);
   display: flex;
   position: relative;

   animation: show .6s ease .1s 1 forwards;

}

@keyframes show{
    0%{
        opacity: 0;
    }
    100%{
        opacity: 1;
    }
}

.form-container__sign-up-form{
    width: 50%;
    background-color: #232328;

    position: relative;
    color: white;
    padding: 120px 50px;
    box-sizing: border-box;
}

.form-container__sign-up-form p {
    font-family: 'Oswald', sans-serif;
    font-size: 18px;
    letter-spacing: 1px;
    margin-bottom: 8px;
}


.form-container__sign-up-form label {
    color: white;
    font-family: 'Oswald', sans-serif;
    font-size: 16px;
    letter-spacing: 1px;
    text-transform: uppercase;
}


.form-container__sign-up-form input[type="checkbox"] {
    position: relative;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    width: 30px;
    height: 15px;
    background-color: #eee;
    border-radius: 20px;
    margin: 0 8px;
    box-shadow: 0 0 10px black;
    transition: .3s;
}


.form-container__sign-up-form input:checked {
    /* background-color: rgb(65, 212, 198); */
    background-color: rgb(170, 214, 210); 
}

.form-container__sign-up-form input[type="checkbox"]::before {
    transition: .3s;
    content: '';
    position: absolute;
    height: 17px;
    width: 17px;
    border-radius: 50%;
    top:-1px;
    left: -4px;
    background-color: #878799;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.445);
}

.form-container__sign-up-form input:checked[type="checkbox"]::before {
    
    left: 16px;

     background-color: rgb(65, 212, 198);
}

.form-container__sign-up-form button {
    display: block;
    margin-top: 80px;
    width: 150px;
    padding: 10px 8px;
    background-color: transparent;
    color: white;
    border: 2px solid white;
    cursor: pointer;
    outline: none;
    letter-spacing: 1px;
    text-transform: uppercase;
    
}

.form-input{
    width: 300px;
    font-family: 'Oswald', sans-serif;
    font-size: 18px;
    letter-spacing: 1px;
    color: white;
    background-color: transparent;
    border: none;
    border-bottom: 1px solid white;
    margin-bottom: 30px;
    outline: none;
    padding: 10px 0;
    transition: .3s;
}

.form-input:focus{
    border-color: rgb(65, 212, 198);
}


.form-container__header{
    position: relative;
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: white;
    font-family: 'Oswald', sans-serif;

}


.form-container__header h1{
    display: flex;
    justify-content: center;
    align-items: center;

}

.under-anim{
    position: absolute;
    height: 1px;
    box-sizing: border-box;
    display: flex;
    justify-content: center;
    align-items: center;
    animation-name: under-anim;
    animation-delay: 1s;
    animation-duration: 2s;
    animation-iteration-count: 1;
    animation-fill-mode: both;
    box-sizing: border-box;
    top:340px;
}

@keyframes under-anim{
    0%{
        width: 0px;
        border-bottom: 2px solid white;
    }
    100%{
        width: 70%;
        border-bottom: 2px solid white;
    }
}

.x-btn{
    position: absolute;
    bottom: -8%;
    right: 1%;
    color: white;
    border: 3px solid white;
    padding: 3px 10px 5px 10px;
    border-radius: 50%;
    cursor: pointer;
    font-weight: bold;
}

/*----------------------------------------------------------*/

.button-wrapper{
    /* border: 1px solid rgb(255, 255, 255); */
    background-color:rgb(13, 13, 26);
    /* box-sizing: content-box; */
    margin-top: 80px;
    height: 50px;
    display: flex;
    justify-content: center;
    text-align: center;
    width: 240px;
    position: relative;
    overflow: hidden;

    left: 50%;

    transform: translateX(-50%);

    cursor: pointer;
    font-family: 'Montserrat', sans-serif;
    font-weight: bold;

    box-shadow: 0 0 10px 5px rgba(0, 0, 0, 0.376);

    
}

.button-wrapper:hover .sign-over{
    top:0px;
    
}

.button-wrapper:hover .sign-up-button{
    /* color: black; */
    transition-delay: .1s;
    
}

.sign-up-button{
    display: flex;
    justify-content: center;
    align-items: center;
    border: none;
    z-index: 2;

}

.sign-over {
    transition: .2s ease-in;
    position: absolute;
    width: 100%;
    height: 50px;
    top:50px;
    background-color: rgb(18, 119, 112); 
    z-index: 1;

}








</style>