<template>
  <section >
    <v-container>
      <v-row>
        <v-col>
            
          <div width="500" height="500" id="myCanvasContainer" onload()>
            <canvas  id="myCanvas">
             
              <ul>
                <li>
                  <a href="http://www.google.com" target="_blank">Google</a>
                </li>
                <li><a href="/fish">Fish</a></li>
                <li><a href="/chips">Chips</a></li>
                <li><a href="/salt">Salt</a></li>
                <li><a href="/vinegar">Vinegar</a></li>
              </ul>
            </canvas>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
  <!-- <span class="tags top-tags"> &nbsp;&nbsp;&nbsp;&lt;body&gt;</span> -->
</template>






    <script>
export default {
  methods: {
     onload() {
        try {
          TagCanvas.Start('myCanvas','tags',{
            textColour: '#ff0000',
            outlineColour: '#ff00ff',
            reverse: true,
            depth: 0.8,
            maxSpeed: 0.05
          });
        } catch(e) {
          // something went wrong, hide the canvas container
          document.getElementById('myCanvasContainer').style.display = 'none';
        }
      }
  },
};
</script>









<style scoped>
#myCanva {
  color: red;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: auto;
  width: auto;
  height: 100%;
}
#myCanvasContainer {
  background-color: rgb(128, 98, 98);
}
</style> > 
