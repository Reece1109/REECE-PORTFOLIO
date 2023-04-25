<template>
  <section id="projects" class="container-fluid">
    <h3 class="display-3 text-white mt-5 mb-5 text-decoration-underline">Projects</h3>
    <div class="container">
    </div>
    <div class="row px-5">
      <div class="col-md-4" v-for="project in projects" :key="project.name">
        <div class="card text-center w-75 m-auto mb-5">
          <img :src="project.image" :alt="project" loading="lazy">
          <div class="card-body">
            <h5 class="card-title">{{ project.title }}</h5>
            <a :href="project.gitHub" target="_blank" class="p-1 m-auto">GitHub</a>
            <a :href="project.netlify" target="_blank" class="p-1 m-auto">N</a>
          </div>
        </div>
      </div>
      <div class="col-md-4" v-for="projectss in projectVue" :key="projectss.name">
        <div class="card text-center w-75 m-auto mb-5">
          <img :src="projectss.image" :alt="projectss" loading="lazy">
          <div class="card-body">
            <h5 class="card-title">{{ projectss.title }}</h5>
            <a :href="projectss.gitHub" target="_blank" class="p-1 m-auto">GitHub</a>
            <a :href="projectss.firebase" target="_blank" class="p-1 m-auto">Firebase</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: 'Portfolio',
          image: 'https://i.postimg.cc/NjJGvgWh/astronaut.gif',
          gitHub: 'https://github.com/Reece1109/Reece-sPortfolio.git',
          netlify: 'https://dashing-bublanina-080d8c.netlify.app'
        },
        {
          title: 'BMI Calculator',
          image: 'https://i.postimg.cc/NjJGvgWh/astronaut.gif',
          gitHub: 'https://github.com/Reece1109/BMI-Calculator.git',
          netlify: 'https://dashing-bublanina-080d8c.netlify.app'
        },~
        {
          title: 'Portfolio',
          image: 'https://i.postimg.cc/NjJGvgWh/astronaut.gif',
          gitHub: 'https://github.com/Reece1109/Reece-sPortfolio.git',
          netlify: 'https://dashing-bublanina-080d8c.netlify.app'
        },
        {
          title: 'Ecommerce Website',
          image: 'https://i.postimg.cc/Fzc9KY0H/sales.gif',
          github: "https://github.com/Reece1109/EcommerceWebsite.git",
          netlify: "https://iridescent-bunny-c9b063.netlify.app"
        },
      ],
    }
  }
}
</script>


<style scoped>

#projects{
  color: #ffffff;
min-height: 100vh;
background-image:
  linear-gradient(#000000da, #000000b7),
  url('../assets/pexels-abhilash-sahoo-4295841.jpg');
background-size: cover;
background-repeat: no-repeat;
background-position: bottom;
overflow-x: hidden;
display: flex;
flex-flow: column nowrap;
justify-content: center;
align-items: center;
font-family: 'Ysabeau', sans-serif;
}
.title {
  text-align: center;
  padding: 25px 0;
}

title p {
  font-size: 18px;
}

.card-body {
  box-shadow: 0 0 20px 7px black;
}

.card {
  margin: 20px 10px;
}

.card-body {
  color: black;
  font-size: 15px;
  font-weight: 600;
}

.card-body a {
  color: rgb(36, 147, 166);
}

.card-body a:hover {
  color: black;
  text-decoration: none;
}

img {
  object-fit: cover;
}</style>