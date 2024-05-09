<template>
    <v-card>
        <v-card-title>
            Students List
            <v-spacer></v-spacer>
            <v-text-field v-model="search" append-icon="mdi-magnify" label="Search" single-line
                hide-details></v-text-field>
        </v-card-title>
        <v-data-table :headers="headers" :items="StudentData" :search="search">
            <template slot="item.actions" slot-scope="{item}">
                <v-btn color="green accent-4"> DELETE</v-btn>
                <v-btn color="red accent-4"> EDIT</v-btn>
            </template>
        </v-data-table>

    </v-card>
</template>

<script>
export default {
  data () {
    return {
      headers: [
        {
          text: 'Student ',
          align: 'start',
          sortable: false,
          value: 'name',
        },
        { text: 'Lastname', value: 'Lastname' },
        { text: 'Firstname', value: 'Firstname' },
        { text: 'Middlename', value: 'Middlename' },
        { text: 'Course', value: 'Course' },
        { text: 'Section', value: 'Section' },
      ],
      desserts: [],
    }
  },
}
</script>
