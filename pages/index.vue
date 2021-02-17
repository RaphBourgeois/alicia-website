<template>
  <div>
  <b-container >
    <b-row>
      <!--<b-col></b-col>-->
      <b-col class="bck">
        <img src="../assets/header2.jpg" />
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

        <b-row>
          <b-col style="text-align: center;"><img src="../assets/background_1_0.5.jpg"/></b-col>
          <b-col>
            <b-row>
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
          <b-col style="text-align: center;">
              <h2>Animation Demos</h2>
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
        <h2>Contact Me</h2>
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
              placeholder="Please describe your project."
              rows="3"
            ></b-textarea>
            <b-button type="submit" variant="primary">Submit</b-button>
            <b-button type="reset" variant="danger">Reset</b-button>
          </b-form>
      </b-col>
      <!--<b-col></b-col>-->
    </b-row>
    
  </b-container>
  </div>
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

.demoBox {
  align-v: center;
}

.test {

  border: 1px solid rgba(86,61,124,1);
}

.navbar {
   margin-left: ($spacer * .25) !important;
}

.bck {
  background-color: Rgba(125,155,155,1);
}
img {
  width: 100%;
  min-width:300px;
  height: auto;
}
</style>
