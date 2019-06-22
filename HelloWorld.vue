<template>
  <div class="hello">

  <h3>Subject List</h3>
  
 
 
 <button id="remove" class="btn btn-danger" @click='deleteTableRow(index)'>Remove</button>
 <button id="add"  class="btn btn-primary"  @click='addTableRow()' >Add New Row</button>
   <table class="table table-hover table-bordered">

    <thead>
    <tr>
      <th scope="col">Subject ID</th>
      <th scope="col">Subject Name</th>
      <th scope="col">Class</th>
      <th scope="col">Board</th>

      <th scope="col">Action</th>
    </tr>
  </thead>
  <tr>
   <td>Maths106</td>
    <td>Maths</td>
      <td>10</td>
        <td>CBSE</td>
         
  <td><button  id="edit" class="btn btn-primary"  @click='deleteTableRow(index)' >Edit</button></td>
    </tr>

    <tr>
   <td>Science1120</td>
    <td>Science</td>
      <td>11</td>
        <td>ICSE</td>
         
  <td><button id="edit" class="btn btn-primary"  @click='deleteTableRow(index)' ><hover strip v-for="items in ">Edit</hover></button></td>
    </tr>

<tr v-for="(content, index) in tableRows">
  <td>Maths106</td>
    <td>Maths</td>
      <td>10</td>
        <td>CBSE</td>
          
  <td><button id="edit" class="btn btn-primary"  @click='deleteTableRow(index)' ><hover strip v-for="items in ">Edit</hover></button></td>
</tr>
</table><br>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {

    return {
         
       tableRows:[ ],
    counter:[ ],
    subs:["a","b","c"]
    }

  },
   
  methods:{
    addTableRow: function () { 
      this.counter++;
      this.tableRows.push(+this.counter);
         this.tableRows.push(+this.counter);
      
   },
    deleteTableRow: function (idx) { 
      this.counter--;
      this.tableRows.splice(idx, 1);      
   }
	}
  
   }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button{
  float:right;
  border-radius:3px;
}
#add{
  background-color:#6e45f7;
  border-size:7px;
}
#edit{
   background-color:#6e45f7;
   
}
</style>
