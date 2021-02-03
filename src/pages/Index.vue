<template>
  <Layout>
    <div id="earth">
    
    </div>
          <g-link to="/about/"><v-btn color="accent" fab>CD</v-btn></g-link>

  </Layout>
</template>



<script>
export default {
  //  data() {
  //     return {
  //       project: [
  //         {
  //          image: require("./images/earth.jpg"),
  //         },
  //       ]
  //     }
  //  },
  metaInfo: {
    title: "About us",
  },
};
</script>





<style >
.v-main__wrap {
    /* background-image: url('https://images2.alphacoders.com/305/thumb-350-30530.jpg'); */
/* background-color: black; */
background-image: url('https://images7.alphacoders.com/671/thumb-1920-671262.jpg');
/* background-image: url("./images/nebuleuse.jpg"); */
}

#earth {

  /* [1] Allow it to contain the absolutely positions pseudo-elements (later-on) */
  position: relative;

  /* [2] Set-up the dimensions and spacing */
  width: 245px;
  height: 245px;
  margin: 3em auto;

  /* [3] Prepare the animation effects */
  transition: transform 200ms linear;
  animation: rotate 50s linear infinite; /* This is going to be defined in the next step */

  /* [4] Tweak the appearance, and give it a nice background i.e. the world map */
  color: #000;
  border-radius: 50%;
  
  background: url("https://lh5.googleusercontent.com/-kkxEx-SkRaY/VBLF4BV2lZI/AAAAAAAAKao/FnKsv7402_c/s500/earthmap.jpg") ;
  /* background: url("http://2amii.org/upmc/2016_VENDREDI_PM/BOURGEOIS/Cirrus_over_Warsaw,_June_26,_2005.jpg") ; */

  /* background: require("./images/groupomania_projet.png") ; */

  box-shadow:  20px 0 80px 6px rgba(0, 0, 0, 1);

  box-shadow: inset 20px 0 80px 6px rgb(204, 200, 200), 0 0 80px white;


  /* [5] Position things in a 3d space */
  transform-style: preserve-3d;
}
#earth:after {
  /* [1] Break the flow to show this as an overlay */
  position: absolute;
  top: 0;
  left: 0;

  /* [2] Make it take all the space available in the box (ahem... globe!) */
  width: 100%;
  height: 100%;

  /* [3] Make sure this has no generated content, as we want this just for fancy purposes */
  content: "";

  /* [4] Give it some shape and shadow */
  border-radius: 50%;
  box-shadow: -80px 15px 80px 10px rgba(0, 0, 0, 0.9) inset;

      opacity: 0.1;
}
#earth:before {
  /* [1] Again, break the flow to show this as an overlay */
  position: absolute;
  top: 0;
  left: 0;

  /* [2] Again, give it all the available space */
  width: 100%;
  height: 100%;

  /* [3] Duh. */
  content: "";

  /* [4] Add some shape and overlay effect to it */
  opacity: 0.2;
  border-radius: 50%;
  background: radial-gradient(circle at 100px 100px, #fff, #000);
}
@keyframes rotate {
  0% {
    background-position: 0 0;
  }
  100% {
    background-position: 630px 0;
  }
}
</style>