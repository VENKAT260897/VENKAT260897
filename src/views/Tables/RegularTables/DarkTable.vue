<template>
  <div>
       <base-header class="pb-0 pb-0 pt-0 pt-md-3 bg-gradient-sucess">
      <b-row>
        <b-col xl="0" md="0">
          <h1>DEV Portal</h1>
         </b-col>
       </b-row>
    </base-header>
  <b-card body-class="p-0" header-class="border-0">
     <template v-slot:header>
    
        <b-row>
          <b-col sm="2">
            <base-input
              type="text"
              label="ID"
              placeholder="id"
              v-model="filterdata.Id">
            </base-input>
          </b-col>
         
          <b-col sm="4">
            <base-input
              type="text"
              label="DESCRIPTION"
              placeholder="description"
              v-model="filterdata.Description">
            </base-input>
          </b-col>
          <b-col sm="4">
            <base-input
              type="text"
              label="CUSTOMER"
              placeholder="customer"
              v-model="filterdata.Customer">
                          </base-input>
          </b-col>
          <b-col sm="2"  align-self="center" >
           <!-- <a href="#!" class="btn btn-sm btn-primary">Search</a>  -->
           <button class="btn btn-primary">Search</button>
          </b-col>
       </b-row>
     </template>
  </b-card>
 </div>
</template>

<script>
  import projects from './../projects'
  import { Table, TableColumn} from 'element-ui'
  export default {
    name: 'light-table',
    components: {
      [Table.name]: Table,
      [TableColumn.name]: TableColumn
    },
    data() {
      return {
        projects,
        currentPage: 1
      };
    }
  }
</script>
