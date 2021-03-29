<template>
  <div>
    <base-header class="pb-0 pb-1 pt-0 pt-md-3 bg-gradient-sucess">
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
              v-model="filterdata.Id"
            >
            </base-input>
          </b-col>

          <b-col sm="4">
            <base-input
              type="text"
              label="DESCRIPTION"
              placeholder="description"
              v-model="filterdata.Description"
            >
            </base-input>
          </b-col>
          <b-col sm="4">
            <base-input
              type="text"
              label="CUSTOMER"
              placeholder="customer"
              v-model="filterdata.Customer"
            >
            </base-input>
          </b-col>
          <b-col sm="2" align-self="center">
            <button class="btn btn-primary" v-on:click="search" v-bind="ID">
              Search
            </button>
          </b-col>
        </b-row>
        <!-- </ejs-grid> -->
      </template>

      <!-- table part-->
      <base-header class="pb-0 pb-1 pt-0 pt-md-3 bg-gradient-sucess">
        <h1 align="center">Issuse Details</h1>
      </base-header>

      <el-table
        class="table-responsive table"
        :data="filterdata"
        header-row-class-name="thead-light"
      >
        <el-table-column label="Id" min-width="80px" prop="Id">
          <template v-slot="{ row }">
            <div class="font-weight-600">{{ row.Id }}</div>
          </template>
        </el-table-column>

        <el-table-column
          label="Description"
          min-width="70px"
          prop="Description"
        >
        </el-table-column>
        <el-table-column label="Customer" min-width="90px" prop="Customer">
        </el-table-column>

        <el-table-column
          label="Entered on"
          min-width="90px"
          v-model="filterdata.Enteredon"
          prop="Enteredon"
        >
        </el-table-column>

        <el-table-column label="Updated on" min-width="90px" prop="Updated on">
          <template v-slot="{ row }">
            <div class="font-weight-600">{{ row.Updatedon }}</div>
          </template>
        </el-table-column>
        <el-table-column>
          <button class="btn btn-primary" @click="gotoView()">View</button>
        </el-table-column>
      </el-table>
    </b-card>
  </div>
</template>
<script>
import {
  Table,
  TableColumn,
  DropdownMenu,
  DropdownItem,
  Dropdown,
} from "element-ui";

export default {
  name: "issuse",
  components: {
    [Table.name]: Table,
    [TableColumn.name]: TableColumn,
    [Dropdown.name]: Dropdown,
    [DropdownItem.name]: DropdownItem,
    [DropdownMenu.name]: DropdownMenu,
  },

  methods: {
    search(item) {
      console.log("search button is pressed");
    },
    gotoView() {
      alert("you preseed view button");
      console.log("view button is pressed");
      this.$router.push("/View");
    },
  },
  computed: {
    filters: {
      Id: { value: " ", key: ["Id"] },
    },
  },

  data() {
    return {
      filterdata: [
        {
          Id: 1,
          Description: "venkat1",
          Customer: "123",
          Enteredon: "12-08-1998",
          Updatedon: "13-09-1995",
         
        },
        {
          Id: 2,
          Description: "venkat2",
          Customer: "222",
          Enteredon: "25-08-1997",
          Updatedon: "28-08-1997",
        },
        {
          Id: 3,
          Description: "venkat3",
          Customer: "333",
          Enteredon: "25-04-2000",
          Updatedon: "28-06-2001",
        },
      ],
    };
  },
};
</script>
<style>
.sidenav {
  width: 130px;
  position: fixed;
  z-index: 1;
  top: 20px;
  left: 10px;
  background: #eee;
  overflow-x: hidden;
  padding: 8px 0;
}
</style>
