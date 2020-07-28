<template>
  <div>
     <b-navbar type="dark" variant="dark">
      <b-navbar-nav>
        <b-nav-item href="#">Converter</b-nav-item>

        <b-nav-item-dropdown text="About" right>
          <b-dropdown-item href="#/profile">Profile</b-dropdown-item>
          <b-dropdown-divider></b-dropdown-divider>
          <b-dropdown-item href="#">Resources</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-navbar>
    <b-tabs card>
      <b-tab title="Binary" active>
        <b-card-text>
              <div class="mt-4">
            <b-card bg-variant="light">
                <b-form-group
                label-cols-lg="3"
                label="Binary to Decimal"
                label-size="lg"
                label-class="font-weight-bold pt-0"
                class="mb-0"
                >
                <b-form-group
                    label-cols-sm="3"
                    label="Binary :"
                    label-align-sm="right"
                    label-for="nested-height"
                >
                    <b-form-input id="nested-height" v-model="binary"></b-form-input>
                </b-form-group>
                </b-form-group>
            </b-card>
        </div>
        <br>
        <div>
            <b-jumbotron lead="Decimal value is :">
                <p><strong>{{binToDec}}</strong></p> 
            </b-jumbotron>
        </div>

        </b-card-text>
      </b-tab>

      <b-tab title="Decimal">
        <b-card-text>
          <div class="mt-4">
            <b-card bg-variant="light">
                <b-form-group
                label-cols-lg="3"
                label="Decimal to Binary"
                label-size="lg"
                label-class="font-weight-bold pt-0"
                class="mb-0"
                >
                <b-form-group
                    label-cols-sm="3"
                    label="Decimal :"
                    label-align-sm="right"
                    label-for="nested-height"
                >
                    <b-form-input id="nested-height" v-model="decimal"></b-form-input>
                </b-form-group>
                </b-form-group>
            </b-card>
        </div>
        <br>
        <div>
            <b-jumbotron lead="Binary value is :">
                <p><strong>{{decToBin}}</strong></p> 
            </b-jumbotron>
        </div>
        </b-card-text>
      </b-tab>
    </b-tabs>
      
  </div>
</template>

<script>
  export default {
    name: 'BinaryToDec',
    data() {
      return {
        binary : null,
        decimal: null
      }
    }, 
    computed:{
        binToDec: function(){
          var str = this.binary;
          var output = parseInt(str,2);
          return output;
          },

          decToBin: function(){
             if (this.decimal !== '') return (this.decimal >>> 0).toString(2);
                return null;

          }


    }
  }
</script>

<style scoped>

   body{
     background:lightgray;
   }
   #main{
   position:absolute;
   top:10%;
   left:23%;
   width:40%;
   background:teal;
   text-align:center;
   padding:6%;
     
   }
   #bin,#dec{
   width:50%;
   margin:1%;
   height:30px;
   font-size:16px;
   font-weight:bold;
   }
   .btn {
  
  width:23%;
  padding:15px;
  margin:10px;
  background:#30160e;
  border:1px solid #30160e;
  color:whitesmoke;
  }
  .lbl {
  
  font-size:16px;
  font-weight:bold;
  font-family:ariel,sans-serif;
  padding:15px;
  }
  
</style>

