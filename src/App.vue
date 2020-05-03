
<template>
  <div id="app" class="small-container">
    <h1 id="head">Employee</h1>

    <employee-form @add:employee="addEmployee" />
    <employee-table :employees="employees" />
  </div>
</template>

<script>
import EmployeeTable from "@/components/EmployeeTable.vue";
import EmployeeForm from "@/components/EmployeeForm.vue";
export default {
  name: "app",
  components: {
    EmployeeTable,
    EmployeeForm
  },
  data() {
    return {
      employees: [
        /*{
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
        */
      ]
    };
  },
  methods: {
    addEmployee(employee) {
      const lastId =
        this.employees.length > 0
          ? this.employees[this.employees.length - 1].id
          : 0;
      const id = lastId + 1;
      const newEmployee = { ...employee, id };
      this.employees = [...this.employees, newEmployee];
    }
  }
};
</script>

<style>
button {
  background: green;
  border: 1px solid darkred;
}

.small-container {
  max-width: 680px;
}
</style>
