<template>
  <section id="techno">
    <h2 class="title">technologies</h2>
    <div class="search">
      <div>
        <p>rechercher une technologie</p>
        <input type="text">
      </div>
    </div>
    <ul>
      <li id="vuejs">
        <div class="logo">
          <img src="https://img.lght.pics/CtEG.png" alt="vuejs">
          <p>Vuejs</p>
        </div>
        <div class="progressBar">
          <div class="percentage" :style="{ 'width': advancedBegginer }"></div>
        </div>
      </li>
      <li id="django">
        <div class="logo">
          <img src="https://img.lght.pics/Ctd9.png" alt="django">
          <p>Django</p>
        </div>
        <div class="progressBar">
          <div :style="{ 'width': intermediate }"></div>
        </div>
      </li>
      <li id="nodejs">
        <div class="logo">
          <img src="https://img.lght.pics/Ctdq.png" alt="nodejs">
          <p>NodeJS</p>
        </div>
        <div class="progressBar">
          <div :style="{ 'width': begginer }"></div>
        </div>
      </li>
      <li id="wordpress">
        <div class="logo">
          <img src="https://img.lght.pics/Ctdy.png" alt="wordpress">
          <p>WordPress</p>
        </div>
        <div class="progressBar">
          <div :style="{ 'width': begginer }"></div>
        </div>
      </li>
      <li id="php">
        <div class="logo">
          <img src="https://img.lght.pics/Ctdm.png" alt="php">
          <p>PHP</p>
        </div>
        <div class="progressBar">
          <div :style="{ 'width': medium }"></div>
        </div>
      </li>
      <li id="js">
        <div class="logo">
          <img src="https://img.lght.pics/CtdM.png" alt="javascript">
          <p>JavaScript</p>
        </div>
        <div class="progressBar">
          <div :style="{ 'width': intermediate }"></div>
        </div>
      </li>
      <li id="scss">
        <div class="logo">
          <img src="https://img.lght.pics/CtdX.png" alt="scss">
          <p>SCSS</p>
        </div>
        <div class="progressBar">
          <div :style="{ 'width': good }"></div>
        </div>
      </li>
      <li id="bootstrap">
        <div class="logo">
          <img src="https://img.lght.pics/Ctd7.png" alt="bootstrap">
          <p>BootStrap</p>
          </div>
        <div class="progressBar">
          <div :style="{ 'width': intermediate }"></div>
        </div>
      </li>
      <li id="jquery">
        <div class="logo">
          <img src="https://img.lght.pics/CtdU.png" alt="jquery">
          <p>JQuery</p>
        </div>
        <div class="progressBar">
          <div :style="{ 'width': intermediate }"></div>
        </div>
      </li>
      <li id="gitkraken">
        <div class="logo">
          <img src="https://img.lght.pics/CtfE.png" alt="gitkraken">
          <p>GitKraken</p>
        </div>
        <div class="progressBar">
          <div :style="{ 'width': good }"></div>
        </div>
      </li>
    </ul>
  </section>
</template>
<script>
  import {i18n} from '@/plugins/i18n.js'
  export default {
    name: 'technoView',
    data() {
      return {
        begginer: '30%',
        medium: '50%',
        advancedBegginer: '60%',
        intermediate: '75%',
        good: '90%'
      }
    }
  }

</script>
