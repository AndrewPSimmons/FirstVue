
<template>
  <div id="app" class="small-container">
    <h1>Employee</h1>

    <employee-table :employees="employees" />
  </div>
</template>

<script>
import EmployeeTable from "@/components/EmployeeTable.vue";
export default {
  name: "component-name",
  components: {
    EmployeeTable
  },
  data() {
    return {
      employees: [
        {
          id: 1,
          name: "Andrew Simmons",
          email: "Andrewps339@gmail.com"
        },
        {
          id: 2,
          name: "Emma Simmons",
          email: "EMS@gmail.com"
        },
        {
          id: 3,
          name: "Jon Doe",
          email: "JDG@gmail.com"
        }
      ]
    };
  }
};
</script>

<style>
button {
  background: lightcyan;
  border: 1px solid darkred;
}

.small-container {
  max-width: 680px;
}
</style>
