<template>
  <b-container >
    <b-row>
      <b-col class="bck">
        <img src="../assets/header2.jpg" />
        <b-navbar toggleable="lg" type="dark" variant="info">
                  <b-navbar-brand href="#">Alicia QB Voice Over</b-navbar-brand>
                  <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                  <b-collapse id="nav-collapse" is-nav>
                    <b-navbar-nav>
                      <b-nav-item href="#commercial">Comercial Demos</b-nav-item>
                      <b-nav-item href="#animation">Animation Demos</b-nav-item>
                      <b-nav-item href="#narration">Narration Demos</b-nav-item>
                      <b-nav-item href="#contact">Contact</b-nav-item>
                    </b-navbar-nav>
                    <!-- Right aligned nav items -->
                    <b-navbar-nav class="ml-auto">
                    
                    </b-navbar-nav>
                  </b-collapse>
          </b-navbar>

        <b-row>
          <b-col style="text-align: center;"><img src="../assets/background_1_0.5.jpg"/></b-col>
          <b-col style="text-align: center;">
              <a id="commercial"><h2>Commercial Demos</h2></a>
              <b-col>
              <audio controls>
                <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
                Your browser does not support the audio tag.
              </audio>
              </b-col>
          </b-col>
        </b-row>
        <b-row>
          <b-col style="text-align: center;"><img src="../assets/background_2_0.5.jpg" /></b-col>
          <b-col style="text-align: center;">
              <a id="animation"><h2>Animation Demos</h2></a>
                <audio controls>
                  <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
                  Your browser does not support the audio tag.
                </audio>
                <audio controls>
                  <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
                  Your browser does not support the audio tag.
                </audio>
                <audio controls>
                  <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
                  Your browser does not support the audio tag.
                </audio>
          </b-col>

        </b-row>
        <b-row>
          <b-col style="text-align: center;"><img src="../assets/background_3_0.5.jpg" /></b-col>
          <b-col style="text-align: center;">
            
              <a id="narration"><h2>Narration Demos</h2></a>
              <b-col>
                <audio controls>
                  <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
                  Your browser does not support the audio tag.
                </audio>
              </b-col>
              <video width="320" height="240" controls>
                <source src="../assets/Making a Difference in Our World360p.mp4" type="video/mp4">
              Your browser does not support the video tag.
              </video>
            
          </b-col>
        </b-row>
        
        <b-row class="text-center" align-v="center">
        <b-col>
          <a id="contact"><img src="../assets/contact.png" style="width: 70%;"/></a>
        </b-col>
        <b-col>
        
        <b-form @submit="onSubmit" @reset="onReset" v-if="show">
            <b-form-group id="input-group-1">
              <b-form-input
                id="input-1"
                v-model="form.email"
                type="email"
                placeholder="Email address"
                required
              ></b-form-input>
            </b-form-group>

            <b-form-group id="input-group-2" >
            </b-form-group>
            <b-textarea
              id="input-2"
              v-model="form.desc"
              filled
              auto-grow
              label="Description"
              required
              placeholder="Please describe your project."
              rows="3"
            ></b-textarea>
            <div class="space">
            <b-button type="submit" variant="primary">Submit</b-button>
            <b-button type="reset" variant="danger">Reset</b-button>
            </div>
          </b-form>
          </b-col>
          </b-row>
          <div style="justify-content: center;text-align:center">
          Thanks to Blabl @blabla for the graphics used in this site
          </div>
      </b-col>
    </b-row>
    
  </b-container>
</template>

<script>
export default {
    data() {
      return {
        form: {
          email:'',
          desc: ''
        },
        show: true
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.form.email = ''
        this.form.desc = ''
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
</script>

<style>

.space {
  margin-top: 100 !important;
}
.bck {
  background-color: Rgba(125,155,155,1);
}
img {
  width: 100%;
  height: auto;
}
video {
  width: 90%;
  height: auto;
}
</style>
