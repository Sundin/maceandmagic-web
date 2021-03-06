<template>
  <main-layout>
    <div class="content">


      <img
        alt="Sound Realms logo"
        class="topImage"
        src="../assets/sound_realms_mace_and_magic.jpg"
      />


      <section>
      <div class="section-content">
        <h1>The first ever REAL audio solo roleplaying game</h1>
        <div class="text">
        <p class="bold">
          Now you can, whenever you have a moment to spare, hear fantastic worlds
          unfold and have an unparalleled solo RPG experience. Now you can
          roleplay more and do not have to rely upon getting your RPG group
          together to sink your sword into a dragons heart or incinerate a
          goblin with a fireball spell!
        </p>
        <p>
          Sound Realms presents <i>Mace & Magic</i>, the first ever real audio solo
          roleplaying game set in a brand new dark fantasy realm bustling with
          adventure, perilous challenges and adversaries.
        </p>
        <p>
          Featuring great adventures, presented with top class voice-over
          performances, original orchestral music, cinematic sound effects,
          digital RPG dice rolls, digital character sheets, skills, spells,
          swords and monsters!
        </p>
        <p>Brace yourself and enter the Realm of <i>MACE & MAGIC</i>!</p>
        </div>
        <img src="../assets/pile_of_bones.png" class="small-image"/>
      </div>
      </section>


      <div class="hero">
        <div class="hero-text">
          <h2 class="inverted">Dare you enter the realm of Mace & Magic?</h2>
          <p class="inverted"> Download the free demo adventure now, and always be rembered as a bold pioneer of adventuring, hero of <i>Mace & Magic</i>!</p>
          <div>
            <Button href="/download">Get Started</Button>
            <Button href="/learn-more" :inverted="true">Learn More</Button>
          </div>
        </div>
        <img
          class="hero-image"
          src="../assets/mace_background.jpg"
        />
      </div>


      <section>
      <div class="section-content">
        <h1>THE Audio Adventure System</h1>
        <p>
          Sound Realms aim to deliver immersive and captivating experiences to the paperback RPG and solo adventure book audience but also to
          offer the regular consumer of audio books or fantasy and sci-fi literature an experience beyond what ordinary audio books can offer.
          Any consumer of mobile games will find Sound Realms interesting since it's game mechanics rely heavily upon the player using their
          imagination to envision what happens in the game. This takes mobile gaming beyond tiny screens and touch fiddling into new realms
          &mdash; Sound Realms.
        </p>
      </div>
      <!-- <div class="gallery"> -->
        <!-- <img src="../assets/dice_and_book.jpg" /> -->
      <!-- </div> -->

      <div class="video-wrap">
        <div class="video-container">
          <iframe
            width="560"
            height="315"
            src="https://www.youtube.com/embed/4FMkHwHB8pM"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
            class="video">
          </iframe>
        </div>
      </div>


      <div class="section-content">
        <div class="row">
          <img src="../assets/dreadhorn.png" class="dreadhorn_image"/>
          <div class="row_column_2 text">
          <p>
            The first release on the Sound Realms platform will be
            <i>Mace & Magic</i>, an audio based solo fantasy roleplaying game.
            A demo adventure is available for game testing by selected parties now for iOS and Android devices.
            We aim to use the free demo as a key element in a forthcoming crowdfunding campaign to release
            an adventure of approximately 7 hours of playing time. <i>Mace & Magic</i> is set in the brand-new world of "Mihr",
            a dark fantasy realm strook by an apocalyptic event called "The Magiklysm",
            making it an ideal environment for epic adventures.
            Production of this adventure has already begun.
          </p>
          <p>
            With <i>Mace & Magic</i> we aim to explore and expand the possibilities of this new format not only in cutting edge programming
            but also in the recording and usage of audio.
            <i>Mace & Magic</i> uses a slightly modified version of Choasium Inc’s RPG rule set "Basic Roleplaying System" (BRP),
            that we have successfully digitalised for a classic RPG experience, complete with dice roles and character sheets etc.
          </p>
          </div>
        </div>
      </div>
      </section>

      <GametestStrip/>
      <Footer/>
    </div>
  </main-layout>
</template>

<script>
import Button from '../components/Button.vue';
import Footer from '../components/Footer.vue';
import MainLayout from '../layouts/Main.vue';

export default {
  name: 'Home',
  components: {
    Button,
    Footer,
    MainLayout,
  },
};
</script>


<style scoped>
.row {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: center;
  max-width: 960px;
}
.text {
  align-items: flex-start;
}
.dreadhorn_image {
  max-width: 40%;
  padding-bottom: 30px;
  padding-right: 30px;
}

.gallery {
  padding-top: 30px;
  padding-bottom: 60px;
  max-width: 80%;
}
.logo {
  padding: 12px;
  max-width: 90%;
  height: auto;
  object-fit: scale-down;
}
.topImage {
  width: 100%;
}
.small-image {
  padding-bottom: 30px;
}


img {
  max-width: 100%;
}

.hero {
  width: 100%;
  position: relative;
}
.hero-image {
  width: 100%;
  min-height: 400px;
}
.hero-text {
  position: absolute;
  top: 50%;
  left: 0;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%
}
.hero-text > p {
  max-width: 60%;
}

.video-wrap {
  width: 80%;
  max-width: 960px;
  padding-top: 60px;
  padding-bottom: 120px;
}

.video-container {
  position: relative;
  overflow: hidden;
  height: 0;
  padding-bottom: 56.25%; /* creates a 16:9 aspect ratio */
}

.video-container iframe,
.video-container embed {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  max-width: 100%;
}

@media screen and (max-width:980px) {
  .row {
    flex-direction: column;
  }
  .dreadhorn_image {
    max-width: 100%;
  }

  .gallery {
    max-width: 95%;
  }
}
@media screen and (max-width:680px) {
  .hero-text {font-size: 0.8rem}
}
@media screen and (max-width:540px) {
  .hero-text {font-size: 0.7rem}
}
</style>
