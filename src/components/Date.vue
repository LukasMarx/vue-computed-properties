<template>
  <div>
    <p>Computed: {{formatedDate}}</p>
    <p>Method: {{formatDate()}}</p>
    <p>{{random}}</p>
  </div>
</template>

<script>
export default {
  name: "Date",
  props: {
    date: Date
  },
  data() {
    return {
      random: 1
    };
  },
  created() {
    setInterval(() => {
      this.random = Math.random();
    }, 500);
  },
  computed: {
    formatedDate() {
      console.log("computed");
      let options = {
        year: "numeric",
        month: "long",
        day: "numeric"
      };
      return this.date.toLocaleString("en-us", options);
    }
  },
  methods: {
    formatDate() {
      console.log("method");
      let options = {
        year: "numeric",
        month: "long",
        day: "numeric"
      };
      return this.date.toLocaleString("en-us", options);
    }
  }
};
</script>