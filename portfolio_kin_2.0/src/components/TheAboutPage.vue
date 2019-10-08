<template>
  <v-container id="aboutme">
    <v-card class="mx-auto d-lg-flex align-center">
      <v-container class="pa-2">
        <div>
          <div class="headline mb-2">About me</div>
          <p>I was born in Vilvoorde, 28/12/1983. My parents are from Hong Kong, China. Growing up, I've always been fascinated by technology and science. I spent a lot of time in the library and loved to play on the computer.</p>
          <p>When I had to choose my studies, I  went the scientific route, because I loved chemistry and doing experiments. But when I started working in a laboratory I quickly found out that studying science and doing a job in science wasn't quite the same thing. I wanted to do something more creative and more tech-related. With the proper retraining, I started to work in the printing sector.</p>
          <p>I really enjoyed my job as a Prepress Coordinator, every project came with  its own set of challenges and it allowed me to be creative at times. But after 9 years, I noticed the printing sector going into a steady decline: there was less work, and the manager asked if I could make a website with a webshop for the company to boost sales. I didn't have  any experience making websites at that point, but was eager to give it a try.</p>
          <p>It took a while and a lot of trial and error but  it was functional, and while I learned a lot in the process, I wanted to be able to do it properly, and perhaps even professionally. When I saw an ad from BeCode for a free training as Junior Web Developer, I instantly knew what my next step was going to be.</p>
        </div>

        <v-card-actions>
          <v-btn
            href="mailto:cheungkin.wong@gmail.com"
            title="cheungkin.wong@gmail.com"
            target="_blank"
            text
          >
            <v-icon>mdi-email</v-icon>
          </v-btn>
          <v-btn
            href="https://www.linkedin.com/in/cheungkin/"
            target="_blank"
            title="https://www.linkedin.com/in/cheungkin/"
            text
          >
            <v-icon>mdi-linkedin-box</v-icon>
          </v-btn>
          <v-btn
            href="https://github.com/cheungkinwong"
            title="https://github.com/cheungkinwon"
            target="_blank"
            text
          >
            <v-icon>mdi-github-box</v-icon>
          </v-btn>
        </v-card-actions>
      </v-container>
      <v-img src="../assets/info.jpg"></v-img>
    </v-card>
  </v-container>
</template>


<script>
export default {
  name: "TheAboutPage",
  data: () => ({
    isActive: false
  })
};
</script>