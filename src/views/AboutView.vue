<template>
  <div class="about w-100 h-100 d-flex align-items-center justify-content-center">
      <div class="about-container p-4 mt-5">
        <div class="about-title-holder d-flex align-items-center pt-4">
          <h4 class="about-title w-25">ABOUT ME</h4>
        </div>
        <div class="about-paragraph-container d-flex flex-column align-items-start ps-3 pt-4 text-black">
          <h3 class="ms-4 greet-text-about">Hello, I am Lazola Makubalo</h3>
          <p class="about-paragraph ps-4">
            I am a software developer based in Cape Town. I love building amazing apps.
            Navigate to my <router-link to="/projects" class="">project section</router-link> to 
            see some of the projects that I have built.
            If you have any project that you need help with. Don't hesitate to <router-link to="/contact">contact</router-link> me.
          </p>
        </div>
        <div class="d-flex what-id-do-container">
          <div class="w-50 h-100 d-flex flex-column align-items-start ps-5 pt-2 web-dev-container">
            <h5 class="web-dev-title decorated">Web Development</h5>
            <p class="text-start skills-text">I develop websites and web applications using various programming languages</p>
          </div>
          <div class="w-50 h-100 d-flex flex-column align-items-start ps-5 pt-2 ui-ux-container">
            <h5 class="ui-ux-title decorated">UI/UX Design</h5>
            <p class="text-start skills-text">I also learnt UI/UX design at LifeChoices</p>
          </div>
        </div>
        <div class="interests-wrapper d-flex flex-column align-items-start ps-5 pt-3">
          <h4 class="decorated text-black interests">Interests</h4>
          <div class="interests-container list-unstyled">
            <li class="py-2 text-start ps-3">
              <i class="bi bi-music-note-beamed icons"></i>
              Music
            </li>
            <li class="py-2 text-start ps-3">
              <i class="bi bi-pencil-fill icons"></i>
              Drawings
            </li>
            <li class="py-2 text-start ps-3">
              <i class="bi bi-book-half icons"></i>
              Reading
            </li>
          </div>
        </div>
      </div>
  </div>
</template>
<script>
export default {
  
}
</script>
<style>
  a.router-link-exact-active {
    text-decoration: none;
    color: black;
  }
  .about-container {
    height: 65%;
    width: 55%;
    background: rgba(255, 255, 255, 0.755);
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr repeat(3, 3fr);
  }

  .about-title {
    scale: .9;
    position: relative;
    z-index: 1;
  }

  .about-title::before, .interests-title::before {
    content: '';
    width: 35px;
    height: 35px;
    background: var(--theme-color);
    border-radius: 50%;
    position: absolute;
    z-index: -1;
    translate: -1rem -.2rem
  }

  .about-paragraph {
    text-align: left;
    width: 90%;
  }

  .decorated {
    position: relative;
    z-index: 1;
  }

  .decorated::before {
    content: '';
    height: 30px;
    width: 30px;
    background: var(--theme-color);
    border-radius: 50%;
    position: absolute;
    translate: -.7rem -.2rem;
    z-index: -1;
  }

  .interests{
    position: relative;
    scale: .95;
  }

  .interests-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 1fr;
    width: 100%;
  }

  .icons {
    padding-right: .5rem;
    scale: 3
  }

  @media screen and (max-width: 800px) {
    a.router-link-exact-active {
      text-decoration: none;
      color: black;
    }
    .about-container {
      height: 78%;
      width: 80%;
      background: rgba(255, 255, 255, 0.755);
      display: grid;
      grid-template-columns: 1fr;
      grid-template-rows: 1fr repeat(3, 3fr);
      overflow: auto;
    }
  
    .about-title {
      scale: .9;
      position: relative;
      z-index: 1;
      margin-left: 2rem;
    }

    .skills-text {
      font-size: 14px;
    }

    .web-dev-title, .ui-ux-title {
      font-size: 19px;
    }
  
    .about-title::before, .interests-title::before {
      content: '';
      width: 35px;
      height: 35px;
      background: var(--theme-color);
      border-radius: 50%;
      position: absolute;
      z-index: -1;
      translate: -1rem -.2rem
    }
  
    .about-paragraph {
      text-align: left;
      width: 90%;
      font-size: 14px;
    }
  
    .decorated {
      position: relative;
      z-index: 1;
    }
  
    .decorated::before {
      content: '';
      height: 30px;
      width: 30px;
      background: var(--theme-color);
      border-radius: 50%;
      position: absolute;
      translate: -.7rem -.2rem;
      z-index: -1;
    }
  
    .interests{
      position: relative;
      font-size: 21px;
    }
  
    .interests-container {
        display: flex;
        gap: 2rem;
   
    }

    .interests-container li{
      padding: 0 !important;
    }
  
    .icons {
      padding-right: .5rem;
      scale: 3
    }
  }

  @media screen and (max-width: 500px) {
    a.router-link-exact-active {
      text-decoration: none;
      color: black;
    }
    .about-container {
      height: 80%;
      width: 95%;
      background: rgba(255, 255, 255, 0.755);
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 0 !important;
    }
  
    .about-title {
      scale: .9;
      position: relative;
      z-index: 1;
      width: 100% !important;
    }

    .greet-text-about {
      scale: .9;
      padding: 0 !important;
      margin: 0 !important;
    }

    .skills-text {
      font-size: 14px;
    }

    .what-id-do-container {
      display: flex;
      flex-direction: column;
    }

    .web-dev-container, .ui-ux-container {
      width: 100% !important;
      display: flex;
      justify-content: center;
    }

    .web-dev-title, .ui-ux-title {
      font-size: 19px;
    }
  
    .about-title::before, .interests-title::before {
      content: '';
      width: 35px;
      height: 35px;
      background: var(--theme-color);
      border-radius: 50%;
      position: absolute;
      z-index: -1;
      translate: -1rem -.2rem
    }
  
    .about-paragraph {
      text-align: left;
      width: 90%;
      font-size: 15px;
      margin-top: 1rem;
      text-align: center;
    }
  
    .decorated {
      position: relative;
      z-index: 1;
    }
  
    .decorated::before {
      content: '';
      height: 30px;
      width: 30px;
      background: var(--theme-color);
      border-radius: 50%;
      position: absolute;
      translate: -.7rem -.2rem;
      z-index: -1;
    }
  
    .interests{
      position: relative;
      font-size: 21px;
    }
  
    .interests-container {
        display: flex;
        padding: 0 !important;
        flex-direction: column;
        gap: 1rem !important;
    }
  
    .icons {
      padding-right: .5rem;
      scale: 3
    }

    .interests-wrapper {
      width: 100% !important;
      margin-bottom: 2rem;
    }
  }

</style>

