<template>
  <div>
    <h1>vue table</h1>
    <p>more demo <a href="https://337547038.github.io/akvue/#/table">https://337547038.github.io/akvue/#/table</a> </p>
    <Table :data="data">
      <TableColumn label="date" prop="date"></TableColumn>
      <TableColumn label="name" prop="name"></TableColumn>
      <TableColumn label="tel" prop="tel"></TableColumn>
      <TableColumn label="address" prop="address"></TableColumn>
      <TableColumn label="control">
        <template slot-scope="scope">
          del
        </template>
      </TableColumn>
    </Table>
  </div>
</template>

<script>
// @ is an alias to /src
import '../assets/_table.scss'
import {Table, TableColumn} from '@/components/table'

export default {
  name: 'home',
  data() {
    return {
      data: [
        {
          date: '2019-01-01',
          name: 'zhang san',
          tel: '138000138',
          address:'address'
        },
        {
          date: '2019-01-02',
          name: 'zhangA',
          tel: '138000138',
          address:'address'
        }
      ]
    }
  },
  components: {
    Table, TableColumn
  }
}
</script>
