<template>
  <div class="condtional-container">
    <p>{{ msg }}</p>
    <hr />
    <div v-if="firstEnabled"> 1st stamenet with v-if flag -- {{ firstEnabled }}</div>
    <hr />

    <button @click="secondDisabled = !secondDisabled">secondDisabled Button :{{ secondDisabled }}</button>
    <div v-if="secondDisabled"> 2nd I stamenet with v-if flag -- {{ secondDisabled }}</div>
    <div v-else> 2nd II stamenet with v-else flag -- {{ secondDisabled }}</div>
    <hr />

    <button @click="type = 'A'">V-else-if A Button - {{ type }}</button>
    <button @click="type = 'B'">V-else-if B Button - {{ type }}</button>
    <button @click="type = 'C'">V-else-if C Button - {{ type }}</button>
    <button @click="type = ''">Reset - {{ type }}</button>
    <div v-if="type === 'A'"> Type A of V-else-if Condition</div>
    <div v-else-if="type === 'B'">Type B of V-else-if Condition</div>
    <div v-else-if="type === 'C'">Type C of V-else-if Condition</div>
    <div v-else> final v-else condition i.e type not A/B/C</div>

    <hr />
    <button @click="vShowEnabled = !vShowEnabled">v-show toggle</button>
    <div v-show="vShowEnabled">v-show div {{ vShowEnabled ? 'enabled' : 'disabled' }}</div>

    <hr />
    <p>template v-if : no additional div tag in dom</p>
    <template v-if="templateVif">
      <h4>Hello</h4>
      <h4>World!</h4>
    </template>

  </div>
</template>


<script>
export default {
  name: 'ConditionalStatements',
  props: {
    msg: String
  },
  data() {
    return {
      firstEnabled: true,
      secondDisabled: false,
      type: '',
      vShowEnabled: true,
      templateVif: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.condtional-container {
  background-color: aliceblue;
  min-height: 90vh;
}
</style>
