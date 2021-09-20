<template>
  <div class="file-manager">
    <h1 class="file-manager__caption">Файловый менеджер</h1>
    <div class="file-manager__data">
      <FolderView name="$" :folders="folders" :files="files" />
    </div>
  </div>
</template>

<script>
import FolderView from './components/FolderView.vue'
import data from './data/list';

export default {
  name: 'App',
  components: {
    FolderView
  },
  data: () => data
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  height: calc(100vh - 30px);
  display: flex;
  align-items: center;
  justify-content: center;

  
}

.file-manager {
  background-color: #f8f7f7;
  box-shadow: 0 0 15px #b6b6b6;

  min-width: 400px;
}

.file-manager__caption {
  font-size: 25px;
  text-align: center;
  padding: 10px;
}

.file-manager__data {
  overflow-y: auto;
  

  height: 500px;

  padding-bottom: 20px;
  // padding-top: 10px;
}

::-webkit-scrollbar {
  width: 5px;
  height: 5px;
}

::-webkit-scrollbar-track {
  background: none;
}

::-webkit-scrollbar-thumb {
  background: none;
  border: 3px solid #b6b6b6;
  border-radius: 3px;
}
</style>
