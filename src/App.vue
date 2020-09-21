<template>
  <div id="app">
    <date @pick="handleDatePick"></date>
    <el-date-picker v-model="value"></el-date-picker>
  </div>
</template>

<script>
import date from './components/calendar/panel/date'

export default {
  name: 'App',
  components: {
    date
  },
  data() {
    return {
      value: ''
    }
  },
  methods: {
    handleDatePick(date) {
      console.log('date', new Date(date).getTime())
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
