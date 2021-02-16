<template>
  <b-container fluid>
  <b-row>
    <b-col></b-col>
    <b-col class="bck">
      <!-- <b-row><img src="../assets/header2.jpg"/></b-row>-->
      <b-navbar toggleable="lg" type="dark" variant="info">
                <b-navbar-brand href="#">Alicia QB Voice Over</b-navbar-brand>
                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                <b-collapse id="nav-collapse" is-nav>
                  <b-navbar-nav>
                    <b-nav-item href="#">Demos</b-nav-item>
                    <b-nav-item href="#">Contact Me</b-nav-item>
                  </b-navbar-nav>
                  <!-- Right aligned nav items -->
                  <b-navbar-nav class="ml-auto">
                  
                  </b-navbar-nav>
                </b-collapse>
        </b-navbar>

      <b-row class="test;">
        <b-col style="text-align: center;"><img src="../assets/background_1_0.5.jpg"/></b-col>
        <b-col>
          <b-row class="test">
            <h2 class="demoBox">Commercial Demos</h2>
          </b-row>
          <b-row>
            <b-col>
              Best way to kill moles!
            </b-col>
            <b-col>
            <audio controls>
              <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
              Your browser does not support the audio tag.
            </audio>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <b-row>
        <b-col style="text-align: center;"><img src="../assets/background_2_0.5.jpg" /></b-col>
        <b-col>
          <b-row>
            <h2>Animation Demos</h2>
          </b-row>
          <b-row>
            <b-col>
              Best way to kill bees!
            </b-col>
            <b-col>
              <audio controls>
                <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
                Your browser does not support the audio tag.
              </audio>
            </b-col>
          </b-row>
        </b-col>

      </b-row>
      <b-row>
        <b-col style="text-align: center;"><img src="../assets/background_3_0.5.jpg" /></b-col>
        <b-col>
          <b-row>
            <h3>Narration Demos</h3>
          </b-row>
          <b-row>
            <b-col>
              Best way to kill cats!
            </b-col>
            <b-col>
              <audio controls>
                <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
                Your browser does not support the audio tag.
              </audio>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <b-row style="justify-content: center;">
        <video width="320" height="240" controls>
          <source src="../assets/Making a Difference in Our World360p.mp4" type="video/mp4">
        Your browser does not support the video tag.
        </video>
      </b-row>
      <b-row><h2>Contact Me</h2></b-row>
      <b-row> 

        <b-text-field
          b-model="email"
          label="email"
        >emailasdfsdaf</b-text-field>
      </b-row>
      <b-row>
        <b-textarea
          filled
          auto-grow
          label="Description"
          value="Please describe your project."
          rows="3"
        ></b-textarea>
      </b-row>
    </b-col>
    <b-col></b-col>
  </b-row>
  </b-container>
</template>

<script>
export default {
    data: () => ({
      email: 'John@doe.com',
      description: 'I am mute, need some voice',
    }),
  }
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.demoBox {
  align-v: center;
}

.test {
  background-color: rgba(86,61,124,.15);
  border: 1px solid rgba(86,61,124,1);
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
.bck {
  background-color: Rgba(125,155,155,1);
}
</style>
