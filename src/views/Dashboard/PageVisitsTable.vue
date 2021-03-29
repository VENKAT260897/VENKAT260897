<template>

  <b-card body-class="p-0" header-class="border-0">
    <template v-slot:header>
      <b-row align-v="center">
        <b-col>
          <h3 class="mb-0">FILTERS</h3>
        </b-col>
        <b-row>
          <b-col lg="10">
            <base-input
              type="text"
              label="ID"
              placeholder="id">
            </base-input>
          </b-col>
        </b-row>
          <b-row>
          <b-col lg="10">
            <base-input
              type="text"
              label="DESCRIPTION"
              placeholder="description">
            </base-input>
          </b-col>
        </b-row>
          <b-row>
          <b-col lg="10">
            <base-input
              type="text"
              label="CUSTOMER"
              placeholder="customer">
            </base-input>
          </b-col>
        </b-row>
        <b-col class="text-right">
          <a href="#!" class="btn btn-sm btn-primary">Search</a>
        </b-col>
      </b-row>
    </template>
 
    <el-table class="table-responsive table"
              :data="tableData"
              header-row-class-name="thead-light">
      <el-table-column label="Page name"
                       min-width="130px"
                       prop="page">
        <template v-slot="{row}">
          <div class="font-weight-600">{{row.page}}</div>
        </template>
      </el-table-column>
      <el-table-column label="ID"
                       min-width="70px"
                       prop="visitors">
      </el-table-column>
      <el-table-column label="DESCRIPTION"
                       min-width="90px"
                       prop="unique">
      </el-table-column>
      <el-table-column label="CUSTOMER"
                       min-width="90px"
                       prop="unique">
      </el-table-column>
       <el-table-column label="ENTERED ON"
                       min-width="90px"
                       prop="unique">
      </el-table-column>

      <el-table-column label="UPDATED ON"
                       min-width="90px"
                       prop="bounceRate">
        <template v-slot="{row}">
          {{row.bounceRate}}
        </template>
      </el-table-column>
    </el-table>
  </b-card>
</template>