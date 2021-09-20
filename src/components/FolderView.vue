<template>
  <a href="#" class="folder">
    <div class="folder__icon"></div> 
    {{name}} 
  </a> 
  <template v-for="folder in folders">
    <FolderView :name="folder.name" :folders="folder.folders" :files="folder.files"/>
  </template>
  <template v-for="file in files">
    <FileView :name="file.name" :type="file.type.replaceAll('/','')" :length="file.length"/>
  </template>
</template>

<script>
import FileView from "./FileView";
export default {
  name: 'FolderView',
  components: {FileView},
  props: {
    name: String,
    folders:Array,
    files:Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.folder{
  color: orangered;
  padding-left: 20px;
  
  margin: 0 0px 15px 0px;

  display: flex;
  align-items: center;

  padding-top: 5px;
  padding-bottom: 5px;

  background-color: #ececec;
}

.folder__icon {
  width: 30px;
  height: 30px;
  margin-right: 5px;

  background-image: url(~@/img/folder.png);
  background-size: 100%;
}

.file + .folder {
  margin-top: 20px;
}

</style>
