<template>
  <div id="testimonialsContainer">
    <h1 class="display-3 my-5 m-auto text-white"> Testimonials</h1> 
    <section id="projects" class="container-fluid">
      <div class="container">
      </div>
      <div class="row px-5">
        <div class="col-md-4" v-for="project in projects" :key="project.name">
          <div class="card text-center w-75 m-auto mb-5">
            <img :src="project.image" :alt="project" loading="lazy" class="image-fluid">
            <div class="card-body">
              <h5 class="card-title">{{ project.title }}</h5>
              <p class="card-title">{{ project.text }}</p>
            </div>
          </div>
        </div>
        <div class="col-md-4" v-for="projectss in projectVue" :key="projectss.name">
          <div class="card text-center w-75 m-auto mb-5">
            <img :src="projectss.image" :alt="projectss" loading="lazy">
            <div class="card-body">
              <h5 class="card-title">{{ projectss.title }}</h5>
              <p class="card-title">{{ projectss.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: 'Maxwill-Isaacs',
          image: 'https://i.postimg.cc/9FRNDGp0/DSC-3588.jpg',
          text: 'Reece shows great leadership skills. Always thinks on his feet and a quick learner. Very eager to learn something new and not afraid to explore outside his comfort zone. Very charasmatic and also confident in the work that he presents.',
        },
        {
            title: "Joel",
            image: "https://i.postimg.cc/tgQcHW9W/Joel-Mukanya-pxsjvq7tothncxrrxmd0dmxnbvis2x953vjs3gt7gm.jpg",
            text: "Reece is a very creative, and well-behaved student. He does enjoy working with his classmates and works well on his project. He has gained a-lot of knowledge of web development, including Bootstrap 5. I will be very delighted to see him get hired."
          },
          {
            title: "Mkhuseli Mkeyiya",
            image: "https://i.postimg.cc/Kv1pkJzt/DSC-3531.jpg",
            text: "Reece is a well articulated young man.  His creative thinking,  reasoning patterns and logic is impressive.  His drive and leadership qualities can only lead to success"
          },
          {
            title: "Brogan",
            image: "https://i.postimg.cc/m2HXnxkQ/me-1.png ",
            text: "Reece is someone who is always seeking to improve on his skills, eagerly engaging to find out more. He has great communication skills and team skills a well, he is someone who is always on time so I regard him as a very punctual person."
          },
          {
            title: "Javier Goodall",
            image: "https://i.postimg.cc/v84sMRmZ/profileme.jpg",
            text: "When it comes to having conversations and soliciting feedback, Reece is an individual who consistently demonstrates a remarkable level of ease and approachability."
          },
          {
            title: "Brandon Swinton",
            image: "https://i.postimg.cc/gc3G2Fv8/IMG-20210822-WA0208.jpg",
            text: "Reece is dedicated to his craft and always looking for ways to improve it and has a tremendous amount of productivity. He is always showing love to those around him"
          }
      ],
    }
  }
}
</script>

<style scoped>

#testimonialsContainer{
  color: lightgray;
  overflow-x: hidden;
  padding-bottom: 5rem;
  background-image:
  linear-gradient(#000000da, #000000b7),
  url('../assets/pexels-abhilash-sahoo-4295841.jpg');
  background-size: cover;
  background-repeat: no-repeat;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
}

h1{
  font-family: 'Lilita One', cursive;
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
  font-family: 'Lilita One', cursive;
  background-color: rgba(255, 255, 255, 0.1);
}

.card-body {
  color: white;
  letter-spacing: 1px;
  font-size: 17px;
  /* font-weight: 600; */
}

.card-body a {
  color: rgb(36, 147, 166);
}

.card-body a:hover {
  color: black;
  text-decoration: none;
}

.img {
  width: 100%;
  height: auto;
  object-fit: cover;
  flex-grow: 1;
}

</style>




<!-- <template>
    <section id="testimonialsContainer">
        <h1 class="display-5 fw-bold text-center mb-3">Testimonials</h1>

            <div class="row g-0">
                <div v-for="test in testimonials" :key="test" class="col-sm-12 col-md-6 col-lg-4 d-flex justify-content-center align-content-center mb-4">
                  <div class="flip-card">
                <figure class="flip-card-inner">
                  <div class="flip-card-front">
                    <img v-bind:src="test.image" alt="Image"/>
                  </div>
                  <div class="flip-card-back">
                    <p>{{ test.text }}</p>
                  </div>
                </figure>
              </div>
                </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
    return {
        testimonials: [
        {
            id: 1,
            name: "Maxwill-Isaacs",
            image: "https://i.postimg.cc/vHc8rXXx/IMG-20210901-141818-127-1.webp",
            text: "Reece shows great leadership skills. Always thinks on his feet and a quick learner. Very eager to learn something new and not afraid to explore outside his comfort zone. Very charasmatic and also confident in the work that he presents."
        },
        {
            id: 2,
            title: "Joel",
            image: "https://i.postimg.cc/Ghbvn8KL/Joel-Profile.jpg ",
            text: "Reece is a very creative, and well-behaved student. He does enjoy working with his classmates and works well on his project. He has gained a-lot of knowledge of web development, including Bootstrap 5. I will be very delighted to see him get hired."
          },
          {
            id: 3,
            title: "Margo Simon",
            image: "https://i.postimg.cc/zBMn5fhS/64f5c3cac76351c4f71946e2271bee93.jpg",
            text: "Reece is a well articulated young man.  His creative thinking,  reasoning patterns and logic is impressive.  His drive and leadership qualities can only lead to success"
          },
          {
            id: 4,
            title: "Brogan",
            image: "https://i.postimg.cc/m2HXnxkQ/me-1.png ",
            text: "Reece is someone who is always seeking to improve on his skills ,eagerly engaging to find out more . He has great communication skills and team skills a well, he is someone who is always on time so I regard him as a very punctual person."
          },
          {
            id: 5,
            title: "Javier Goodall",
            image: "https://i.postimg.cc/v84sMRmZ/profileme.jpg",
            text: "Reece is a very creative, and well-behaved student. He does enjoy working with his classmates and works well on his project. He has gained a-lot of knowledge of web development, including Bootstrap 5. I will be very delighted to see him get hired."
          },
          {
            id: 6,
            title: "Brandon Swinton",
            image: "https://i.postimg.cc/gc3G2Fv8/IMG-20210822-WA0208.jpg",
            text: "Reece is dedicated to his craft and always looking for ways to improve it and has a tremendous amount of productivity. He is always showing love to those around him"
          }
        ]
        }
    }
}
</script>

<style>
#testimonialsContainer{
  color: lightgray;
  overflow-x: hidden;
  padding-bottom: 5rem;
  background-image:
  linear-gradient(#000000da, #000000b7),
  url('../assets/pexels-abhilash-sahoo-4295841.jpg');
  background-size: cover;
  background-repeat: no-repeat;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
}
.flip-card {
    background-color: transparent;
    width: 20em;
    height: 25em;
    border-radius: 1.5em;
  }
  .flip-card .flip-card-inner .flip-card-front img,
  .flip-card .flip-card-inner .flip-card-back{
    border-radius: 1.5em;
  }

.flip-card-front img{
    object-fit: cover;
    object-position: center;
    width: 100%;
    height: 100%;
}

  .flip-card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: all 0.5s ease-in-out;
    transform-style: preserve-3d;
  }
  
  .flip-card:hover .flip-card-inner {
    transform: rotateY(180deg);
  }
  
  .flip-card-front, .flip-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
  }
  
  .flip-card-front {
    color: black;
  }
  
  .flip-card-back {
    padding: 0.5em;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: var(--darkCOLOR);
    color: var(--highlightCOLOR);
    transform: rotateY(180deg);
  }

  img{
    width: 100%;
  }
</style> -->
