<template>    
    <a href="#" class="file" :title="['Open file: ', name]">
      <div :class="['file__icon', type]"></div> 
        {{name}} 
        <span class="file__size">({{length}} Кб)</span>
    </a>  
</template>

<script>
export default {
  name: 'FileView',
  props: {
    name: String,
    type: String,
    length: String
  }
}
</script>

<style scoped lang="scss">
.file {
  margin: 8px 40px;

  display: flex;
  align-items: center;
  color: green;
  font-size: 16px;
}

.file__icon {
  width: 30px;
  height: 30px;
  margin-right: 5px;

  background-image: url(~@/img/file.png);
  background-size: 100%;
}

.file__size {
  margin-left: 5px;
  font-size: 10px;
}

.imagesvg {
  background-image: url(~@/img/svg.png);
}

.imagesvg {
  background-image: url(~@/img/svg.png);
}

.imagejpeg {
  background-image: url(~@/img/jpeg.png);
}

.imagepng {
  background-image: url(~@/img/png.png);
}

.applicationjavascript {
  background-image: url(~@/img/js.png);
}

.applicationjson {
  background-image: url(~@/img/json.png);
}
</style>
