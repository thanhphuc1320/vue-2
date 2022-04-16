<template>
  <div class="list">
    <div v-for="(language, index) in languages" 
    :key="index" @click="language.selected = !language.selected" 
    :class="{selector: language.selected}"
    >
        <span>{{ language.content }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      languages: [
        { content: 'php', selected: false },
        { content: 'html', selected: false },
        { content: 'css', selected: false },
        { content: 'reactjs', selected: false },
        { content: 'vuejs', selected: false },
      ],
    };
  }
};
</script>

<style>
.list div{
  display: inline-block;
  border: 2px solid blue;
  padding: 20px 50px;
  margin: 10px 8px;
  border-radius: 8px;
  cursor: pointer;
}
.list div.selector {
  background-color: greenyellow;
  
}
.list div.selector {
  background-color: green;
  
}
</style>