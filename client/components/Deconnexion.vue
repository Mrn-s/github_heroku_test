<template>

  <div v-if="checkIfLogged(user_medecin.id, user_patient.id)"></div>

</template>

<script>
  module.exports = {
    props: {
      user_medecin:{type: Object },
      user_patient: {type: Object }
    },
    data () {
      return {

      }
    },
    methods: {
      checkIfLogged(user_medecin, user_patient) {
        if (user_medecin != '' || user_patient != '') {
          this.$emit('logout');
        }
      }
    }
  }
</script>
