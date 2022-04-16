<template>
  <div id="app">
    <!-- <form action=""  @submit.prevent="newtask = ''">
    <input type="text" v-model="newtask" >
    <button @click="addTask()"> Them</button>
    <div v-for="(task, index) in tasks" :key="index">
      <input type="checkbox" v-model="task.done">
      <span :class="{daChon: task.done}">{{task.content}}</span>
    </div></form> -->
    <!-- <span v-if="show"> {{content}} </span>
    <br>
    <p v-show="show"> adsadadsad </p>
    <button @click="show = !show">Bam phat la an</button> -->
    <!-- <input type="radio" id="cac-mon-rau" value="Các món rau" v-model="picked" />
    <label for="cac-mon-rau">Các món rau</label><br />
    <input
      type="radio"
      id="cac-mon-thit"
      value="Các món thịt"
      v-model="picked"
    />
    <label for="cac-mon-thit">Các món thịt</label><br />
    <span>Đã chọn: {{ picked }}</span> -->
    <!-- <select v-model="selected" multiple>
      <option disabled value="">Vui long chon</option>
      <option>aiiiiiijjj</option>
      <option>asdsdsadsaasd</option>
      <option>aassssss</option>
    </select>
    <br>
    <span>Da chon: {{selected}}</span> -->
    <select v-model="selected">
      <option v-for="option in options" v-bind:key="option" v-bind:value="option.value">
        {{option.text}} 
      </option>
    </select>
    <span>Gia tien: {{selected}}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // newtask: '',
      // tasks : [
      //   {content:'hihi', done: false},
      //   {content:'huhuu', done: false},
      //   {content:'hahah', done: false},
      // ]
      // content: "Dong nay show",
      // show: true,
      // picked:''
      // selected:''
      selected: 'Chon qua',
      options: [
        {text: 'assssss', value: '45k'},
        {text: 'aaasssss', value: '35k'},
        {text: 'aadfdsdddsss', value: '25k'},
      ]
    };
  },
  methods: {
    addTask: function () {
      this.tasks.push({ content: this.newtask, done: false });
    },
  },
  watch: {
    newtask: function (newvalue, oldvalue) {
      console.log(oldvalue);
      console.log(newvalue);
      console.log("-------------------------");
    },
  },
};
</script>

<style>
.daChon {
  display: inline-block;

  /* text-decoration-line: line-through; */
}

.chonStyle {
  font-size: 20px;
}
</style>
