<template>
    <div class="random-picker">
        <button @click="trigger">GOOOOO</button>
        <p>{{displayName}}</p>
    </div>
</template>

<script>

export default {
  name: 'random-picker',   
  data () {
    return {
        ongoing: false,
        displayName: '2312312',
        interval: false,
        nameList: ['AA','BBB','CCCC','dddd','ee','fffffff','gggg','hhhh','uuu']
    }
  },
  watch: {
      ongoing (val) {
          if(val === true) {
              this.interval = setInterval(() => {
                  this.displayName = this.nameList[Math.floor(Math.random() * 9)]
                  console.log(this.displayName)
              }, 30);
          } else {
              clearInterval(this.interval);
          }
      }
  },
  methods: {
      trigger () {
          this.ongoing = !this.ongoing
      }
  }
}
</script>

<style>
p {
    font-size: 36px;
    font-weight: bold;
}
</style>
