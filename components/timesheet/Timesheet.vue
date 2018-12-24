<template>
  <b-form-row>
    <b-col>
      <timesheet-day :day="'mon'" />
    </b-col>
    <b-col>
      <timesheet-day :day="'tue'" />
    </b-col>
    <b-col>
      <timesheet-day :day="'wed'" />
    </b-col>
    <b-col>
      <timesheet-day :day="'thu'" />
    </b-col>
    <b-col>
      <timesheet-day :day="'fri'" />
    </b-col>
    <template v-if="wkndVisible">
      <b-col>
        <timesheet-day :day="'sat'" />
      </b-col>
      <b-col>
        <timesheet-day :day="'sun'" />
      </b-col>
    </template>
  </b-form-row>
</template>

<script>
  import TimesheetDay from "./TimesheetDay";

  export default {
    name: "Timesheet",
    components: {TimesheetDay},
    data() {
      return {
        wkndVisible: false,
      }
    },
  }
</script>

<style scoped>

</style>
