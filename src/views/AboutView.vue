<template>
  <div>
    <div class="header">
      <h1>My Portfolio</h1>
    </div>
    <div class="container">
      <div class="intro">
        <h2>{{ name }}</h2>
        <p>{{ intro }}</p>
      </div>
      <div class="skills">
        <div class="skill" v-for="skill in skills" :key="skill">{{ skill }}</div>
      </div>
      <div v-for="project in projects" :key="project.title" class="project">
        <h2>{{ project.title }}</h2>
        <p>{{ project.description }}</p>
        <button><a :href="project.link" target="_blank" rel="noopener noreferrer">Click here</a></button>
      </div>
      <div class="contact">
        <p>Contact me at:</p>
        <p>Email: {{ email }}</p>
        <p>StudentID: {{ studentid }}</p>
        <p>Phone: {{ phone }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'GURDARSHAN KAUSHIK',
      intro: 'Welcome to my portfolio website. Here you can find information about me and my projects.',
      studentid: 'S223153972',
      skills: ['HTML', 'CSS', 'JavaScript', 'Vue.js'],
      projects: [
        {
          title: 'Project 1',
          description: 'In this assignment, we explored responsive web design. We have created a responsive website. We also used the concept of JavaScript.',
          link: 'https://github.com/Gkaushik24/SIT120_1.2P'
        },
        {
          title: 'Project 2',
          description: 'In this task, we created a Todo app using HTML, CSS, and Vue 3. We also created a webpage using Vue 3 concepts.',
          link: 'https://github.com/Gkaushik24/SIT120_2.1C'
        },
        {
          title: 'Project 3',
          description: 'In this task, we created a project proposal report for a cricket survey.',
          link: 'https://github.com/Gkaushik24/SIT120_2.2C'
        },
      ],
      email: 'gurdarshan24k@gmail.com',
      phone: '0424XXXXXX'
    };
  }
};
</script>

<style scoped>
body {
  background-color: #f7f7f7;
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

.header {
  background-color: #333;
  color: #fff;
  padding: 20px 0;
}

.header h1 {
  font-family: 'Tilt Prism', cursive;
  margin: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  box-sizing: border-box;
}

.intro {
  background-color: #fff;
  border-radius: 5px;
  padding: 20px;
  margin: 20px 0;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.intro h2 {
  font-family: 'Pacifico', cursive;
  color: #333;
}

.skills {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.skill {
  background-color: #007bff;
  color: #fff;
  padding: 8px 16px;
  margin: 5px;
  border-radius: 3px;
  text-transform: uppercase;
  font-weight: bold;
}

.project {
  border: 1px solid #ccc;
  padding: 20px;
  margin: 20px 0;
  background-color: #fff;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.project h2 {
  margin-top: 0;
  color: #333;
  font-family: 'Pacifico', cursive;
}

.project p {
  color: #555;
}

.project button {
  background-color: #4CAF50;
  color: #fff;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  margin-top: 10px;
  border-radius: 5px;
  transition-duration: 0.4s;
  font-weight: bold;
}

.project button:hover {
  background-color: #45a049;
}

.contact {
  margin-top: 20px;
  background-color: #fff;
  border-radius: 5px;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.contact p {
  margin: 10px 0;
}

.contact a {
  color: #007bff;
  text-decoration: none;
}

.contact a:hover {
  text-decoration: underline;
}

@media (max-width: 768px) {
  .project {
    padding: 10px;
    margin: 10px 0;
  }
}
</style>
