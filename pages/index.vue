<template>
  <b-container>
    <b-row cols="1" class="bck">
      <b-col>
      <b-row>
        <img src="../assets/header2.jpg" style="width: 100%; height: 38%;"/>
      </b-row>
        <b-navbar toggleable="lg" type="dark" class="navbar-custom"  style="margin-left: -15px;margin-right: -15px;">
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

        <b-row  align-v="center">
          <b-col style="text-align: center;"><img class="img_col" src="../assets/part1.png"/></b-col>
          <b-col style="text-align: center;">
              <a id="commercial"><h2>Commercial Demos</h2></a>
              </br>
              <audio controls>
                <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
                Your browser does not support the audio tag.
              </audio>
          </b-col>
        </b-row>
        <b-row align-v="center">
          <b-col style="text-align: center;"><img class="img_col"  src="../assets/part2.png" /></b-col>
          <b-col style="text-align: center;">
              <a id="animation"><h2>Animation Demos</h2></a>
              </br>
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
        <b-row align-v="center">
          <b-col style="text-align: center;"><img class="img_col"  src="../assets/part3.png" /></b-col>
          <b-col style="text-align: center;">
            
              <a id="narration"><h2>Narration Demos</h2></a>
              </br>
                <audio controls>
                  <source src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_5MG.mp3" type="audio/mpeg">
                  Your browser does not support the audio tag.
                </audio>
              <video width="320" height="240" controls>
                <source src="../assets/Making a Difference in Our World360p.mp4" type="video/mp4">
              Your browser does not support the video tag.
              </video>
            
          </b-col>
        </b-row>
        
        <b-row align-v="center" cols-md="2" cols-sm="1" cols-xs="1">
          <b-col style="text-align: center;"><a id="contact"><img src="../assets/contact.png" class="img_col" /></a></b-col>
          <b-col style="text-align: center;">
            <b-form @submit="onSubmit" v-if="show">
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
                <b-textarea
                id="input-2"
                v-model="form.desc"
                filled
                auto-grow
                label="Description"
                required
                placeholder="Please describe your project."
                rows="4"
                ></b-textarea>
              </b-form-group>
              
              <div class="space">
                <b-button type="submit" variant="primary">Send</b-button>
              </div>
            </b-form>
          </b-col>
        </b-row>
        <div style="justify-content: center;text-align:center">Thanks to Yejin Choi for the graphics used in this site</div>
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
        this.messages = []
        this.triggerSendMessageFunction()
      },

      resetForm(){
        this.form.email = ''
        this.form.desc = ''
      },
      async triggerSendMessageFunction () {
          try {
            const response = await this.$axios.$post('/.netlify/functions/send-contact-email', {
              contactName: 'horse with no name',
              contactEmail: this.form.email,
              message: this.form.desc
            })
            this.resetForm()
            this.messages.push({ type: 'success', text: response })
          } catch (error) {
            this.messages.push({ type: 'error', text: error })
          }
        }
    }
  }
</script>

<style>
.row-compact {
  margin-left: 0;
  margin-right: 0;
  > [class^="col"] {
    padding-left: 0;
    padding-right: 0;
  }
}

.navbar-custom { 
    background-color: #74a6c5 !important; 
} 
.space {
  margin-top: 100 !important;
}
.bck {
  background-color: lightblue;
}
.img_col {
  width: 80%;
  min-width: 300px;
  height: auto;
}
video {
  width: 90%;
  height: auto;
}
</style>
