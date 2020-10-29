<template>
  <div id="aboutContainer">
    <div id="aboutParagraphContainer">
      <p>
        {{ aboutData.professionalParagraph }}
      </p>
      <p>
        {{ aboutData.personalParagraph }}
      </p>
    </div>
    <div id="aboutImgContainer">
      <img :src="aboutData.image" alt="Image of Codey." />
      <h2>{{ aboutData.name }}</h2>
      <p>{{ aboutData.email }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      aboutData: {
        professionalParagraph: `Hello! I am Codey McDaniel and I am a Fullstack Web Developer. I attended the 
          University of Utah's Full Stack Web Development Bootcamp and it was the best decision I made. I have 
          also completed two certificates of completion for Web Development & Programming and Computer Science 
          Fundamentals through Salt Lake Community College.`,
        personalParagraph: `In my free time I like to program, always trying to improve and get better. 
          I am also learning the Python programming language to further improve my skills and broaden my 
          range of programming abilities. When I'm not programming I am either at the gym, out around the 
          valley exploring with my son.`,
        image: "../images/codeyImg.JPG",
        name: "Codey McDaniel",
        email: "codeymcdaniel@gmail.com",
      },
    };
  },
};
</script>

<style scoped>
#aboutContainer {
  display: flex;
  font-size: 1.2em;
  justify-content: space-between;
  flex-direction: column-reverse;
  width: 90%;
  background-color: #336b87;
  border-radius: 15px;
  padding-bottom: 1em;
  margin: 5em auto;
  height: 100%;
  width: 100%;
}
#aboutImgContainer {
  text-align: center;
  padding: 1em;
}
#aboutParagraphContainer p {
  margin: 3em 1em;
  text-align: center;
}
img {
  border-radius: 50%;
}

@media only screen and (min-width: 760px) {
  #aboutContainer {
    flex-direction: row;
    width: 80%;
  }
}
@media only screen and (min-width: 470px) {
  #aboutContainer {
    width: 90%;
  }
}
@media only screen and (min-width: 980px) {
  #aboutContainer {
    width: 65%;
  }
  #aboutImgContainer img {
    padding-top: 2em;
  }
}
</style>
