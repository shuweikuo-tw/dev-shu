<template>
  <div>
    <Header />
    <section id="home" class="hero">
      <h1>I'm a Web Developer</h1>
      <p><kbd>Cmd</kbd> + <kbd>C</kbd> and <kbd>Cmd</kbd> + <kbd>V</kbd></p>
    </section>
    <section id="about">
      <h2>About Me</h2>
      <p>This is the about section.</p>
    </section>
    <section id="portfolio">
      <h2>Portfolio</h2>
      <div class="project" v-for="project in projects" :key="project.id">
        <img :src="project.image" :alt="project.title">
        <p>{{ project.description }}</p>
      </div>
    </section>
    <section id="contact">
      <h2>Contact</h2>
      <ContactForm />
    </section>
    <Footer />
  </div>
</template>

<script>
import AppHeader from '~/components/App/AppHeader.vue';
import ContactForm from '~/components/ContactForm.vue';
import AppFooter from '~/components/App/AppFooter.vue';

export default {
  components: {
    AppHeader,
    ContactForm,
    AppFooter
  },
  data() {
    return {
      projects: [
        { id: 1, image: 'project1.jpg', title: 'Project 1', description: 'Project 1 Description' },
        { id: 2, image: 'project2.jpg', title: 'Project 2', description: 'Project 2 Description' }
      ]
    };
  }
};
</script>

<style scoped>
body {
  background-color: #121212;
  color: #ffffff;
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

p {
  font-size: 36px;
}

.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #1f1f1f;
  text-align: center;
}

h1, h2 {
  color: #bfbfbf;
}

kbd {
  background-color: #eee;
  border-radius: 3px;
  border: 1px solid #b4b4b4;
  box-shadow:
    0em 0px 0px 0px rgba(0, 0, 0, 0) inset,
    -0.07em -0.1em 3px 0px rgb(0 0 0 / 35%) inset;
  color: #333;
  display: inline-block;
  font-size: .85em;
  font-weight: 700;
  line-height: 1;
  padding: 2px 4px;
  white-space: nowrap;
}

.project img {
  width: 100%;
  height: auto;
}

footer {
  background-color: #1f1f1f;
  padding: 1rem;
  text-align: center;
}
</style>
