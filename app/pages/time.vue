<template>
  <div>
    <h1>{{ receivedTime }}秒</h1>
  </div>
</template>

<script>
import { setInterval } from 'timers';
export default {
  data: function() {
    return {
      time: 0.0,
    };
  },
  computed: {
    receivedTime: function() {
      return (Math.round(this.time * 100) / 100).toFixed(2).toString();
    },
  },
  mounted: function() {
    if (process.client) {
      setInterval(
        obj => {
          obj.time += 0.01;
        },
        10,
        this,
      );
    }
  },
};
</script>
