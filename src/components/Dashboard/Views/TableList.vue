<template>
  <div class="content">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12">
          <Card>
            <template slot="header">
              <h5 class="title">Striped Table with Hover</h5>
              <p class="category">Here is a subtitle for this table</p>
            </template>
            <div class="table-responsive table-full-width">
              <n-table class="table table-hover table-striped"
                       :columns="table1.columns"
                       :data="table1.data">

              </n-table>
            </div>
          </Card>

        </div>

        <div class="col-md-12">
          <Card class="card-plain">
            <template slot="header">
              <h5 class="title">Table on Plain Background</h5>
              <p class="category">Here is a subtitle for this table</p>
            </template>
            <div class="table-responsive table-full-width">
              <n-table class="table table-hover"
                       :columns="table1.columns"
                       :data="table1.data">

              </n-table>
            </div>
          </Card>
        </div>

      </div>
    </div>
  </div>
</template>
<script>
  import NTable from 'src/components/UIComponents/Table.vue'
  import Card from 'src/components/UIComponents/Cards/Card.vue'
  const tableColumns = ['Id', 'Name', 'Salary', 'Country', 'City']
  const tableData = [{
    id: 1,
    name: 'Dakota Rice',
    salary: '$36.738',
    country: 'Niger',
    city: 'Oud-Turnhout'
  },
  {
    id: 2,
    name: 'Minerva Hooper',
    salary: '$23,789',
    country: 'Curaçao',
    city: 'Sinaai-Waas'
  },
  {
    id: 3,
    name: 'Sage Rodriguez',
    salary: '$56,142',
    country: 'Netherlands',
    city: 'Baileux'
  },
  {
    id: 4,
    name: 'Philip Chaney',
    salary: '$38,735',
    country: 'Korea, South',
    city: 'Overland Park'
  },
  {
    id: 5,
    name: 'Doris Greene',
    salary: '$63,542',
    country: 'Malawi',
    city: 'Feldkirchen in Kärnten'
  }]

  export default {
    components: {
      NTable,
      Card
    },
    data () {
      return {
        table1: {
          title: 'Stripped Table',
          subTitle: 'Here is a subtitle for this table',
          columns: [...tableColumns],
          data: [...tableData]
        },
        table2: {
          title: 'Table on Plain Background',
          subTitle: 'Here is a subtitle for this table',
          columns: [...tableColumns],
          data: [...tableData]
        }
      }
    }
  }

</script>
<style>

</style>
