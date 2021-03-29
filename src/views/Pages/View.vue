<template>
  <div>
    <base-header class="pb-0 pb-1 pt-0 pt-md-3 bg-gradient-sucess">
      <h1 align="center">View Details</h1>
    </base-header>
        <b-card body-class="p-0" header-class="border-0">
      <template v-slot:header>
        <b-row>
          <b-col sm="4">
            <base-input
              type="text"
              label="ID"
              placeholder="id"
              v-model:="filterdata.Id"
            >
            </base-input>
          </b-col>

          <b-col sm="4">
            <base-input
              type="text"
              label="DESCRIPTION"
              placeholder="description"
              v-model:="filterdata.Description"
            >
            </base-input>
          </b-col>
          <b-col sm="4">
            <base-input
              type="text"
              label="TEAM"
              placeholder="customer"
              v-model:="filterdata.Customer"
            >
            </base-input>
          </b-col>
        </b-row>
        <b-row>
          <b-col sm="4">
            <base-input
              type="text"
              label="STATUS WEIGHT"
              placeholder="STATUS WEIGHT"
              v-model:="filterdata.STATUSWEIGHT"
            >
            </base-input>
          </b-col>

          <b-col sm="4">
            <base-input
              type="text"
              label="ORGCODE"
              placeholder="ORGCODE"
              v-model:="filterdata.ORGCODE"
            >
            </base-input>
          </b-col>
          <b-col sm="4">
            <base-input
              type="text"
              label="STATUSDESCRIPTION"
              placeholder="STATUSDESCRIPTION"
              v-model:="filterdata.STATUSDESCRIPTION"
            >
            </base-input>
          </b-col>
        </b-row> </template
      ><br />
    </b-card>
    <!--notes part-->
    <base-header class="pb-0 pb-1 pt-0 pt-md-3 bg-gradient-sucess">
      <h1 align="center">Notes Details</h1>
    </base-header>
    <b-card body-class="p-0" header-class="border-0">
      <template v-slot:header>
        <b-row>
          <b-col sm="6">
            <base-input type="text" label="Enteredon" placeholder="Entered on" v-model:="filterdata.Notesenteredon">
            </base-input>
          </b-col>

          <b-col sm="6">
            <base-input type="text" label="Updated on" placeholder="Updated on" v-model:="filterdata.Notesupdatedon">
            </base-input>
          </b-col>
        </b-row>
        <b-row>
          <b-col sm="12">
            <base-input
              type="text"
              label="Notes Description"
              placeholder="NotesDescription"
              v-model:="filterdata.NotesDescription"
            >
            </base-input>
          </b-col>
        </b-row>
      </template>
    </b-card>
    <!-- <issue /> -->
  </div>
</template>
    
           
           

  
<script>


export default {
  name: "View",
  components: {
     
  },
  
  data() {
    return {
      filterdata:[ {
        Id: "/argon/",
        Description: "4,569",
        Customer: "340",
        Enteredon: "46,53%",
        Updatedon: "19.25",
        STATUSWEIGHT: "25",
        ORGCODE: "11",
        STATUSDESCRIPTION: "chsghsahchdavcjdabvkbda",
        Notesenteredon:"25-09-2019",
        Notesupdatedon:"26-10-2019",
        NotesDescription:"ghgSGGDJSHAJCHJSAHLHC"
      },
      {
         Id: "1",
        Description: "4,569",
        Customer: "340",
        Enteredon: "46,53%",
        Updatedon: "19.25",
        STATUSWEIGHT: "25",
        ORGCODE: "11",
        STATUSDESCRIPTION: "chsghsahchdavcjdabvkbda",
        Notesenteredon:"25-09-2019",
        Notesupdatedon:"26-10-2019",
        NotesDescription:"ghgSGGDJSHAJCHJSAHLHC"
      }
      ],
    };
  },
};
</script>
<style>


</style>


