<template>
  <div class="container">
    <div class="header">
      <HeaderComponent />
    </div>
    <div class="content-row1-left">
      <PropsButton title="Transform your brand"
        mensage="We are a full-service creative agency specializing in helping brands grow fast. Engage your clients through compelling visuals that do most of the markenting for your."/>
    </div>
    <div class="content-row1-right">
      <img class="imagemOvo" src="./assets/img/image-transform.jpg" alt="imagem ilustrativa de um ovo" srcset="">
    </div>
    <div class="content-row2-left">
      <img class="imagemRosa" src="./assets/img/image-stand-out.jpg" alt="imagem ilustrativa rosa">
    </div>
    <div class="content-row2-right">
      <PropsButton title="Stand out to the right audience"
        mensage="Using a collaborative formula of designers, researchers, photographers, videographers, and copywriters, we'll build and extend your brand in digital places.">
    </PropsButton>
    </div>

    <div class="content-row3-left imagemCereja">
      <ComponentFrutas title="Graphic Design"
        mensage="Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential clients' attention.">
      </ComponentFrutas>
    </div>
    <div class="content-row3-right imagemLaranja">
      <ComponentFrutas title="Photography"
        mensage="Increase your credibility by getting the most stunning, high-quality photos that improve your business image">
      </ComponentFrutas>
    </div>
    <div class="content-row4-left">
      <div class="mainClient">
      <div class="clientUser">
        <h1>CLIENT TESTIMONIALS</h1>
      </div>
      <div class="userPerfil">
      <PerfilUser imgSrc="src/assets/img/image-emily.jpg"
        mensage="We put our trust in Sunnyside and they delivered, making sure our needs were met and deadlines were always hit."
        nomeTitle="Emily R." userTitle="Marketing Director"></PerfilUser>
      <PerfilUser imgSrc="src/assets/img/image-thomas.jpg"
        mensage="Sunnyside's enthusiasm coupled with their keen interest in our brand's success made it a satisfying and enjoyable experience."
        nomeTitle="Thomas S." userTitle="Chief Operating Officer"></PerfilUser>
      <PerfilUser imgSrc="src/assets/img/image-jennie.jpg"
        mensage="Incredible end result! Our sales increased over 400% when we worked with Sunnyside. Highly recommended!"
        nomeTitle="Jennie F." userTitle="Business Owner"></PerfilUser>
      </div>
      </div>

      <div class="imagesColoridas">
        <Section8 imageSrc="src/assets/img/image-gallery-milkbottles.jpg"></Section8>
        <Section8 imageSrc="src/assets/img/image-gallery-orange.jpg"></Section8>
        <Section8 imageSrc="src/assets/img/image-gallery-cone.jpg"></Section8>
        <Section8 imageSrc="src/assets/img/image-gallery-sugarcubes.jpg"></Section8>
      </div>

    </div>
    <div class="footer">
      <h1 class="sunnyTitle">sunnyside</h1>
      <div class="buttonService">
      <button>About</button>
      <button>Services</button>
      <button>Projects</button>
      </div>
      <div class="iconsLogo">
        <ul>
          <li><img src="./assets/icons/icon-facebook.svg" alt="imagem ilustrativa logo facebook"></li>
        </ul>
        <ul>
          <li><img src="./assets/icons/icon-instagram.svg" alt="imagem ilustrativa logo instagram"></li>
        </ul>
        <ul>
          <li><img src="./assets/icons/icon-twitter.svg" alt="imagem ilustrativa logo twitter"></li>
        </ul>
        <ul>
          <li><img src="./assets/icons/icon-pinterest.svg" alt="imagem ilustrativa logo pinterest"></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script scoped>
import HeaderComponent from './components/moleculas/HeaderComponent.vue';
import PropsButton from './components/moleculas/PropsButton.vue';
import PropsImage from "./components/moleculas/PropsImage.vue";
import ComponentFrutas from './components/moleculas/ComponentFrutas.vue';
import PerfilUser from "./components/moleculas/PerfilUser.vue";
export default {
  name: 'App',
  components: { HeaderComponent, PropsButton, PropsImage, ComponentFrutas, PerfilUser },
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

.sunnyTitle{
    font-family: "Barlow", sans-serif;
    font-weight: 800;
    font-size: 40px;
    text-align: center;
    color: hsl(166, 40%, 35%);
}

.mainClient{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.userPerfil{
  grid-area: section7;
  display: flex;
  
}
.clientUser{
  text-align: center;
  color: hsl(220, 2%, 66%);
  padding: 0.3rem;
}

.imgPerfilClient {
  border-radius: 50%;
  width: 5rem;
}

.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto;
  grid-template-areas:
    "header header"
    "section1 section2"
    "section3 section4"
    "section5 section6"
    "section7 section7"
    "footer footer";
}

.header {
  grid-area: header;
  background-color: hsl(200, 100%, 62%);
  height: calc(100vh - 5rem);
}

.content-row1-left {
  grid-area: section1;
}

.content-row1-right {
  background-color: #643f07;
  grid-area: section2;
}

.content-row2-left {
  background-color: #093705;
  grid-area: section3;
}

.content-row2-right {
  background-color: #fff;
  grid-area: section4;
}

.content-row3-left {
  grid-area: section5;
}

.content-row3-right {
  grid-area: section6;
}

.content-row4-left {
  grid-area: section7;
}

.section8 {
  background-color: yellow;
  grid-area: section8;
}

.footer {
  grid-area: footer;
  background-color: hsl(167, 44%, 70%);
  padding: 4rem;
}

.buttonService{
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 60px;
  padding: 50px;
  background: transparent;
}
.buttonService button{
  background: transparent;
  border: none;
  color: hsl(167, 30%, 45%);
  font-weight: 600;
  font-size: 1rem;
  cursor: pointer;
}

.iconsLogo{
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1.5rem;
  padding: 20px;
  cursor: pointer;
  list-style: none;
}

.iconsLogo li{
  list-style: none;
}
.imagemOvo {
  width: 100%;
  height: 100%;
}

.content-row1-left {
  display: flex;
  align-items: center;
  justify-content: center;
}

.content-row2-right {
  display: flex;
  align-items: center;
  justify-content: center;
}

.imagemRosa {
  width: 100%;
  height: 100%;
}

.content-row3-left,
.content-row3-right {
  display: flex;
  align-items: flex-end;
  flex-direction: column;
  height: calc(100vh - 5rem);
}

.imagemCereja {
  background-image: url("./assets/img/image-graphic-design.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}

.imagemLaranja {
  background-image: url("./assets/img/image-photography.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
</style>
