<template>

</template>

<script>
  export default {
    name: "BreakPopup",
    props: {
      id: String,
      modalShow: {
        type: Boolean,
        default: false,
      }
    },
    computed: {
      // modalVisible() {
      //   return this.modalShow;
      // }
    },
    watch: {
      // 'modalShow': function(newValue, oldValue) {
      //   debugger;
      //   this.modalVisible = newValue;
      // }
    },
    methods: {
      handleOk(e) {
        e.preventDefault();
        this.$emit('submittedModal');
        alert(this.id);
      },
      handleCancel(e) {
        e.preventDefault();
        this.$emit('cancelledModal');
        alert(this.id);
      }
    },

  }
</script>

<style scoped>

</style>
