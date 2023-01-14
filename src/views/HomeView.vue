<template>
  <div class="home-page">
    <SocialIcons/>
    <main class="main-content d-flex flex-column align-items-start justify-content-center text-white">
      <h2 class="greet-text"> <span class="text-theme-color">Hi</span>, I am</h2>
      <h1 class="full-name text-theme-color animate__animated animate__bounce">Lazola Makubalo</h1>
      <p class="description">I am an aspiring fullstack developer.</p>
      <router-link to="/about">
        <button class="btn-more py-2">More</button>
      </router-link>
    </main>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  components: {
    
}
}
</script>

<style scoped>
  .home-page {
    background-size: cover;
    object-fit: cover;
    background-position: center;
    height: 100vh;
    scroll-margin: 0vh;
  }

  .main-content {
    height: 100vh;
    padding: 15rem;
  }

  .greet-text {
    font-size: 30px;
  }

  .full-name {
    font-size: 65px;
    margin: 1rem 0 .5rem 0;
  }

  p {
    font-size: 22px;
    text-align: start;
    margin-bottom: 3rem;
  }

  .btn-more {
    width: 200px;
    background: none;
    border: 2px solid var(--theme-color);
    color: var(--theme-color);
    font-size: 20px;
    position: relative;
    box-sizing: border-box;
  }

  @media screen and (max-width: 800px) {
    .home-page {
      background-size: cover;
      object-fit: cover;
      background-position: center;
      height: 100vh;
    }
  
    .main-content {
      height: 100vh;
      padding: 6rem;
    }
  
    .greet-text {
      font-size: 25px;
    }
  
    .full-name {
      font-size: 50px;
      margin: 1rem 0 .5rem 0;
    }
  
    p {
      font-size: 18px;
      text-align: start;
      margin-bottom: 3rem;
      
    }
  
    .btn-more {
      width: 150px;
      background: none;
      border: 2px solid var(--theme-color);
      color: var(--theme-color);
      font-size: 20px;
      position: relative;
      box-sizing: border-box;
      padding: .2rem !important;
    }

    @media screen and (max-width: 500px) {
      .home-page {
        background-size: cover;
        object-fit: cover;
        background-position: center;
        height: 100vh;
        scroll-margin: 0vh;
      }
    
      .main-content {
        height: 100vh;
        padding: 1rem;
        display: flex;
        align-items: center !important;
        gap: 1rem;
      }
    
      .greet-text {
        font-size: 24px;
      }
    
      .full-name {
        font-size: 30px;
        margin: 1rem 0 .5rem 0;
      }
    
      p {
        font-size: 20px;
        text-align: center;
        margin-bottom: 3rem;
        width: 50%;
      }
    
      .btn-more {
        width: 120px;
        background: none;
        border: 1px solid var(--theme-color);
        color: var(--theme-color);
        font-size: 15px;
        position: relative;
        padding: .4rem !important;
        border-radius: 5px;
        box-sizing: border-box;
      }
    }
  }

</style>
