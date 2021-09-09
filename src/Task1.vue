<template>
    <div class="container">
    <div class="card-wrapper">
      <div class="card-wrapper-2">

     
      <div class="card">
        <img src="../public/imgs/john-doe.jpg" class="card-img">
        <h1 class="card-heading">John Doe</h1>
        <p class="card-paragraph"><i class="fas fas-rignt">"</i>  Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit non dicta  minima inventore sit magni dolorum dolor mollitia nesciunt harum veniam ad voluptatem, molestias voluptate hic quas corporis esse? Eaque!
        <i class="fas fas-left">"</i>
        </p>
        <ul class="card-icons">
          <li>
            <a href="#" class="card-icon-link">
              <img src="../public/imgs/vk.png" class="icon">
              <i class="card-icon fab fa-facebook-icon">
              </i>
            </a>
          </li>
          <li>
            <a href="#" class="card-icon-link">
              <img src="../public/imgs/fb.png" class="icon">
              <i class="card-icon fab fa-facebook-icon">
              </i>
            </a>
          </li>
          <li>
            <a href="#" class="card-icon-link">
              <img src="../public/imgs/instagram.png" class="icon">
              <i class="card-icon fab fa-facebook-icon">
              </i>
            </a>
          </li>
          <li>
            <a href="#" class="card-icon-link">
              <img src="../public/imgs/twitter.png" class="icon">
              <i class="card-icon fab fa-facebook-icon">
              </i>
            </a>
          </li>
        </ul>
        <button class="card-btn">View Profile</button>
      </div>

     </div>

    </div>
  </div>
</template>

<script>

export default {
    name: 'Task1.vue',
    components: {

    },

};


</script>

<style >

@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:ital,wght@1,300&display=swap');

*{
  margin: 0px;
  padding: 0px;
}

.card-wrapper-2 {
  position: absolute;
  margin-top: -800px;
}

.container {
    font-family: 'Montserrat', sans-serif;
    height: 100vh;
    width: 100vw;
    background: linear-gradient(rgba(0,0,0,0.4),rgba(0,0,0,0.4)),url('../public/imgs/bg.jpg') no-repeat center; 
}

.icon{
  height: 42px;
  width: auto;
  border-radius: 50%;
  margin: 5px;
  transition: .2s ease;
  box-shadow: 0px 0px 10px 3px rgb(0, 0, 0, 0.2);
}

.icon:hover{
  transform: scale(1.1);
  box-shadow: 0px 0px 15px 5px rgb(0, 0, 0, 0.2);

}
.card-wrapper {
  overflow: hidden;
  box-sizing: border-box;
  position: absolute;
  transform: translate(-50%, -50%);
  left: 50%;
  top: 50%;
  height: 656px;
  width: 450px;
  /* border: 1px solid white; */
  transition: .2s;
  border-radius: 10px;
  background: linear-gradient(rgba(0,0,0,0.4),rgba(0,0,0,0.4)),url('../public/imgs/bg.jpg') no-repeat center;
}

@media (max-height: 950px) {
  .card-wrapper{
    transform: translate(-50%, -60%);
  }
}

/* @media (max-height: 950px) {
  .card-wrapper{
    transform: translate(-50%, -55%);
  }
} */

.card-wrapper:hover{
  box-shadow: 0 0 30px #fff;
  transition: .2s;
}

.card-wrapper:hover .card-wrapper-2{
  transition: 1s;
  margin-top: 0px;
}

.card {

  height: 100%;
  width: 100%;
  background-color: #fff;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  background: linear-gradient(45deg, #EECFBA, #C5DDE8);
}

.card-img{
  height: 300px;
  width: 300px;
  border: 3px solid white;
  padding: 10px;
  object-fit: cover;
  border-radius: 50%;
  margin-top: 15px;
  box-shadow: 0 0 10px 5px rgba(95, 95, 95, 0.37);
  
}

.card-heading {
  font-size: 32px;
  margin: 15px;
  font-weight: 600;
  border-radius: 10px;
  width: 60%;
  display: flex;
  justify-content: center;
  padding: 5px 15px;
  background-color: rgb(255, 255, 255);

  transform: perspective(1000px) skewX(-20deg) rotateY(40deg) translate(20px, 0px);
}

.card-paragraph {
  font-size: 16px;
  padding: 0px 15px;
  font-style: italic;
  text-align: center;
}

.card-icons {
  list-style: none;
  display: flex;
  flex-direction: row;
  padding: 10px;
}

.card-btn {
  border: none;
  outline: none;
  width: 190px;
  font-family: 'Josefin Sans', sans-serif;
  font-size: 20px;
  height: 45px;
  border-radius: 20px;
  margin-bottom: 20px;
  color: white;
  background-color: rgb(88, 46, 12);
  box-shadow: 0 0 10px 5px rgba(95, 95, 95, 0.17);
  transition: .3s;
  cursor: pointer;
}

.card-btn:hover{
  color: black;
  background-color: white;

  transform: scale(1.05);
}



</style>