<template>
  <div>
    <b-form>
      <b-card
        :header="day.toUpperCase()"
      >
        <b-form-row class="mb-sm-1">
          <b-col cols="4">
            <label for="inTime" class="mr-sm-2">IN</label>
          </b-col>
          <b-col>
            <b-form-input id="inTime" type="text" size="sm"></b-form-input>
          </b-col>
        </b-form-row>
        <b-form-row class="mb-sm-1">
          <b-col cols="4">
            <label for="outTime" class="mr-sm-2">OUT</label>
          </b-col>
          <b-col>
            <b-form-input id="outTime" type="text" size="sm"></b-form-input>
          </b-col>
        </b-form-row>
        <b-form-row class="mb-sm-1">
          <b-col>
            <b-button
              class="break-btn"
              size="sm"
              variant="outline-primary"
              @click.prevent="showModal = true"
            >break</b-button>
          </b-col>
        </b-form-row>
      </b-card>
    </b-form>
    <b-modal
      v-model="showModal"
    >
      Testing the modal
    </b-modal>
  </div>
</template>

<script>
  import BreakPopup from "./BreakPopup";
  export default {
    name: "TimesheetDay",
    components: {BreakPopup},
    props: {
      day: {
        type: String,
        default: ''
      }
    },
    data() {
      return {
        showModal: false,
      }
    }

  }
</script>

<style scoped>
  .card-body {
    padding: 0.5em;
  }

  .break-btn {
    width: 100%;
  }
</style>
