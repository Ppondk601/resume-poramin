<template>
  <div class="container">
    <div class="header">
      <Header />
    </div>
    <div class="hiddenMenu">
      <header-media />
    </div>

    <div class="hero-section" id="section1">
      <content class="left-section">
        <ImageInHero />
      </content>
      <content class="right-section">
        <div class="top">
          <TextInHero />
        </div>
        <div class="bottom">
          <CircleButton />
        </div>
      </content>
    </div>


    <div class="resume-section" id="section2">
      <headerOfSection>
        <h2>RESUME</h2>
      </headerOfSection>
      <CardInfo />
    </div>
    <div class="skills-section" id="section3">
      <div class="class-title">
        <h2>SKILLS</h2>
      </div>
      <div class="class-content">
        <CardSkill />
      </div>
    </div>
    <div class="contact-section" id="section4">
      <headerOfSection>
        <h2>CONTACT</h2>
      </headerOfSection>
      <div class="mainContent">
        <Contact />
      </div>
    </div>
    <div class="footer">
    </div>
  </div>
</template>

<script>
import headerMedia from '../components/headerMedia.vue'
export default {
  components: { headerMedia },

}
</script>

<style lang="scss">
html {
  scroll-behavior: smooth;
  scroll-snap-type: y mandatory;
  overflow-y: scroll;
}

body {

  background-color: #293242;
  animation: transitionIn 2s;

  @keyframes transitionIn {
    from {
      opacity: 0;
      transform: translateY(10%);
    }

    to {
      opacity: 1;
      transform: translateY(-50px);
    }
  }


  .container {
    display: flex;
    flex-direction: column;
    margin-left: auto;
    margin-right: auto;

    .header {
      width: 100%;
      display: flex;
      position: sticky;
      top: 0;
      justify-content: center;
      align-items: center;
      z-index: 120;
    }

    .hiddenMenu {
      visibility: hidden;
    }


    .hero-section {
      width: 100%;
      max-height: 750px;
      height: 700px;
      display: flex;
      flex-direction: row;
      align-items: center;
      margin: 3%; //*** */
      justify-content: center;
      border-bottom: 1px solid white;
      scroll-snap-align: center;
      z-index: 1;
      animation: transitionIn 2s;

      @keyframes transitionIn {
        from {
          opacity: 0;
          transform: translateY(-50%);
        }

        to {
          opacity: 1;
          transform: translateY(-50px);
        }
      }

      scorll-snap-m .left-section {
        padding-right: 80px;
        padding-top: 3%;
      }

      .right-section {
        display: flex;
        flex-direction: column;
        padding-left: 10%;

        .top {
          margin-top: 5%;
        }

        .bottom {
          margin-top: 1%;
        }
      }
    }

    .resume-section {
      width: 100%;
      max-height: 750px;
      height: 700px;
      display: flex;
      flex-direction: column;
      scroll-snap-align: start;
      border-bottom: 1px solid white;

      headerOfSection {
        color: white;
        display: flex;
        justify-content: center;
        align-content: center;
        font-size: 24px;
        margin-top: 7%;
      }

    }



    .skills-section {
      width: 100%;
      max-height: 750px;
      height: 700px;
      display: flex;
      flex-direction: column;
      scroll-snap-align: center;
      border-bottom: 1px solid white;
      justify-content: center;

      .class-title {
        display: flex;
        justify-content: center;
        color: white;
        font-size: 24px;
        margin-top: 5%; //*** */

      }

      .class-content {
        display: flex;
        justify-content: center;
      }
    }

    .contact-section {
      width: 100%;
      height: 600px;
      scroll-snap-align: center;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      max-height: 600px;
      position: relative;

      headerOfSection {
        color: white;
        display: flex;
        flex-direction: row;
        font-size: 24px;
        width: 100%;
        position: absolute;
        top: 20%;
        justify-content: center;
      }

      .mainContent {
        margin-top: 100px;
        display: flex;
        flex-direction: row;
      }

    }

    .footer {
      width: 100%;
      height: 50px;
      background-color: #F7D07A;
    }
  }
}

@media only screen and (max-width:992px) and (min-width:601px) {
  html {
    display: flex;
    flex-direction: column;
    margin: 0;
    padding: 0;
    width: 100%;
  }

  body {
    max-width: 992px;
    width: 100%;
    display: flex;
    width: 992px;

    .container {
      max-width: 992px;
      width: 100%;
      display: flex;
      flex-direction: column;
      position: relative;
      scroll-snap-align: none;
      overflow: hidden;
      margin-left: auto;
      margin-right: auto;

      .header {
        display: flex;
      }

      .hiddenMenu {
        display: flex;
        position: fixed;
        top: 1%; //*** */
        left: 3%; //*** */
        z-index: 100;
        visibility: visible;
        width: 100%;
      }

      .hero-section {
        width: 100%;
        display: flex;
        flex-direction: row;
        height: 600px;
        height: 100%;
        align-items: center;
        justify-content: center;
        border-bottom: none;
        position: relative;
        scroll-snap-align: none;
        padding-bottom: 120px;
        margin: 5% 0 0 0; //*** */
        border-bottom: 1px solid white;

        .left-section {
          display: flex;
          justify-content: center;
          padding: 5% 2% 0% 0%; //*** */
          margin-left: 1%;

        }

        .right-section {
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          margin: 0;
          position: relative;
          padding: 50px; //*** */


          .top {
            margin-top: 0px;
            padding-bottom: 40px; //*** */
            border-top: 1px solid white;
            padding-top: 10px; //*** */
            width: 115%;

          }

          .bottom {
            margin: 0;
            border-bottom: 1px solid white;
            display: flex;
            position: absolute;
            justify-content: center;
            padding-bottom: 40px; //*** */
            top: 120px;

          }
        }
      }

      .resume-section {
        width: 100%;
        display: flex;
        flex-direction: column;
        scroll-snap-align: start;
        border-bottom: 1px solid white;
        padding-bottom: 400px;
        margin-bottom: 100px;

        headerOfSection {
          color: white;
          display: flex;
          justify-content: center;
          align-content: center;
          font-size: 24px;
          margin-top: 80px; //*** */
        }

      }

      .skills-section {
        width: 100%;
        display: flex;
        flex-direction: column;
        scroll-snap-align: center;
        border-bottom: 1px solid white;
        justify-content: center;
        padding-bottom: 100px;

        .class-title {
          display: flex;
          justify-content: center;
          color: white;
          font-size: 24px;
          margin-top: 60px; //*** */

        }

        .class-content {
          display: flex;
          justify-content: center;
          width: 100%;
        }
      }

    }
  }
}

@media only screen and (max-width:600px) {
  html {
    display: flex;
    flex-direction: column;
    margin: 0;
    padding: 0;
  }

  body {
    max-width: 600px;
    width: 600px;
    margin: 0;
    padding: 0;
    overflow: hidden;

    .container {
      width: 600px;
      max-width: 600px;
      display: flex;
      flex-direction: column;

      .header {
        display: flex;
      }

      .hiddenMenu {
        visibility: visible;
        display: flex;
        position: fixed;
        top: 20px;
        left: 50px;
        z-index: 100;
      }

      .hero-section {
        display: flex;
        flex-direction: column;
        height: 800px;
        height: 70%;
        align-items: center;
        border-bottom: none;
        position: relative;
        scroll-snap-align: none;
        padding-bottom: 25px; //*** */
        max-width: 600px;
        width: 600px;
        margin: 80px 0px 80px 0px;

        .left-section {
          display: flex;
          justify-content: center;
        }

        .right-section {
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          margin: 0;
          position: relative;
          padding: 0px;


          .top {
            margin-top: 0px;
          }

          .bottom {
            margin: 0;
            border-bottom: 1px solid white;
            display: flex;
            position: absolute;
            justify-content: center;
            padding-bottom: 40px;
            top: 80px;

          }
        }
      }

      .resume-section {
        display: flex;
        scroll-snap-align: none;
        height: 100%;
        border-bottom: 1px solid white;
        padding-bottom: 700px;
        position: relative;
        max-width: 600px;
        width: 600px;

        headerOfSection {
          padding: 0px;
          margin-top: 20px; //*** */
        }
      }

      .skills-section {
        scroll-snap-align: none;
        max-width: 600px;
        width: 600px;
        margin-top: 0px;
        padding: 0px 0px 120px 0px; //*** */

        .class-title {
          margin-bottom: 0px;
          padding: 0px;
        }

        .class-content {
          margin: 0px;
          padding-bottom: 30px; //*** */
        }
      }

      .contact-section {
        scroll-snap-align: none;
        display: flex;
        max-width: 600px;
        width: 600px;
        margin: 0px;
        padding: 0px;
        max-height: 800px;
        justify-content: center;
        flex-direction: column;

        headerOfSection {
          margin: 0px;
          padding: 0px;
        }
      }

      .footer {
        width: 100%;
        height: 50px;
      }
    }
  }
}
</style>