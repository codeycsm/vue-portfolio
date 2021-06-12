<template>
  <div id="portfolioContainer">
    <h1>Portfolio</h1>
    <div id="projectsContainer">
      <div
        class="project"
        v-for="(project, index) in portfolioData"
        :key="index"
      >
        <h3>{{ project.title }}</h3>
        <p class="projectDescription">
          {{ project.description }}
        </p>
        <h5>Technologies</h5>
        <ul>
          <li v-for="(technology, index) in project.technologies" :key="index">
            {{ technology }}
          </li>
        </ul>
        <div>
          <p class="projectButtons">
            <a :href="project.link" target="_blank">Try Me</a>
            <a :href="project.repo" target="_blank">Repo</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      portfolioData: [
        {
          title: "Book Search",
          description:
            "Search google books api to find your favorite books and save them for later or buy.",
          technologies: [
            "Vue.js",
            "HTML",
            "CSS",
            "Express.js",
            "Mongoose.js",
            "MongoDB",
            "Axios",
          ],
          link: "https://book-search-example.herokuapp.com/",
          repo: "",
        },
        // {
        //   title: "Click Game",
        //   description:
        //     "Click the images to earn points but dont click on the same image twice.",
        //   technologies: ["HTML", "CSS", "JavaScript", "React"],
        //   link: "https://codeycsm.github.io/clicky-game/",
        //   repo: "https://github.com/codeycsm/clicky-game ",
        // },
        // {
        //   title: "Fast Track",
        //   description:
        //     "A fasting timer to track your fast time and past fasting data.",
        //   technologies: [
        //     "HTML",
        //     "CSS",
        //     "Materialize",
        //     "JavaScript",
        //     "jQuery",
        //     "NodeJs",
        //     "ExpressJs",
        //     "HandlebarsJs",
        //     "Sequelize",
        //     "MySQL Database",
        //   ],
        //   link: "https://secret-stream-44126.herokuapp.com/timer",
        //   repo: "https://github.com/codeycsm/fast-track",
        // },
        // {
        //   title: "News Scraper",
        //   description:
        //     "Scrapes news articles from local news site, you can save, comment, and delete articles.",
        //   technologies: [
        //     "HTML",
        //     "CSS",
        //     "Bootstrap",
        //     "JavaScript",
        //     "jQuery",
        //     "Node",
        //     "Express",
        //     "Handlebars",
        //     "Axios",
        //     "Cheerio",
        //     "Mongoose",
        //     "MongoDB",
        //   ],
        //   repo: "https://github.com/codeycsm/news-scraper",
        //   link: "https://quiet-meadow-33903.herokuapp.com/",
        // },
        // {
        //   title: "Sequelized Burger List",
        //   description:
        //     "Create a list of burgers you want to eat. Now stored using Sequelize",
        //   technologies: [
        //     "Handlebars",
        //     "jQuery",
        //     "Node",
        //     "Express",
        //     "MySQL",
        //     "Sequelize",
        //   ],
        //   repo: "https://github.com/codeycsm/sequelizeBurger",
        //   link: "https://glacial-castle-91166.herokuapp.com/",
        // },
        // {
        //   title: "Burger Bucket List",
        //   description:
        //     "Create a list of burgers you want to eat and store them in a MySQL database",
        //   technologies: [
        //     "Handlebars",
        //     "jQuery",
        //     "Node",
        //     "Express",
        //     "MySQL",
        //     "ORM",
        //   ],
        //   repo: "https://github.com/codeycsm/burger",
        //   link: "https://pure-ravine-29988.herokuapp.com/",
        // },
        // {
        //   title: "Friend Finder",
        //   description: "Find a friend based on your survey questions.",
        //   technologies: [
        //     "HTML",
        //     "Bootstrap",
        //     "jQuery",
        //     "Express JS",
        //     "Node JS",
        //   ],
        //   repo: "https://github.com/codeycsm/friendFinder",
        //   link: "https://sleepy-refuge-89429.herokuapp.com/",
        // },
        // {
        //   title: "Gif Search",
        //   description:
        //     "Search GIF's from the Giphy API with preset buttons or custom search, Search setitngs quantity and rating as well.",
        //   technologies: [
        //     "HTML",
        //     "CSS",
        //     "Bootstrap",
        //     "JavaScript",
        //     "jQuery",
        //     "Giphy API",
        //   ],
        //   link: "https://codeycsm.github.io/GifSearch/",
        //   repo: "https://github.com/codeycsm/GifSearch",
        // },
        // {
        //   title: "Rock Paper Scissors Multiplayer",
        //   description:
        //     "Play a game of Rock, Paper, Scissors against another player.",
        //   technologies: [
        //     "HTML",
        //     "CSS",
        //     "Bootstrap",
        //     "JavaScript",
        //     "jQuery",
        //     "Firebase",
        //   ],
        //   link: "https://codeycsm.github.io/RPS-Multiplayer/index.html",
        //   repo: "https://github.com/codeycsm/RPS-Multiplayer",
        // },
      ],
    };
  },
};
</script>

<style scoped>
h1 {
  margin: 2em auto;
  color: #fff;
  text-align: center;
}
#portfolioContainer {
  height: 100%;
  width: 100%;
}
#projectsContainer {
  width: 95%;
  margin: 0 auto;
  text-align: center;
  padding: 0.2em 0 0.2em 0;
}
.project {
  background-color: #336b87;;
  border: 1px solid 000;
  color: #fff;
  width: 95%;
  margin: 1em auto;
  padding: 0.3em 0;
  border-radius: 10px;
  height: 24em;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.projectDescription {
  padding: 1em;
}
.project ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}
.project ul li {
  padding: 2em 1em;
  display: inline;
}

.projectButtons {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  padding-top: 1em;
}

.projectButtons a {
  color: #fff;
  text-decoration: none;
}
@media only screen and (min-width: 500px) {
  .project {
    width: 70%;
  }
}
@media only screen and (min-width: 750px) {
  #projectsContainer {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
  .project {
    width: 45%;
  }
}
@media only screen and (min-width: 900px) {
  .project {
    width: 30%;
  }
}
</style>
