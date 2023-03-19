<template>
  <div class="components-container">
    <aside>
      Based on <a class="link-type" href="https://github.com/rowanwins/vue-dropzone"> dropzone </a>.
      DropzoneJS是一个提供文件拖拽上传并且提供图片预览的开源类库,它是轻量级的，不依赖任何其他类库（如JQuery）并且高度可定制.
    </aside>
    <div class="editor-container">
      <dropzone id="myVueDropzone" url="https://httpbin.org/post" @dropzone-removedFile="dropzoneR" @dropzone-success="dropzoneS" />
    </div>
  </div>
</template>

<script>
import Dropzone from '@/components/Dropzone'

export default {
  name: 'DropzoneDemo',
  components: { Dropzone },
  methods: {
    dropzoneS(file) {
      console.log(file)
      this.$message({ message: 'Upload success', type: 'success' })
    },
    dropzoneR(file) {
      console.log(file)
      this.$message({ message: 'Delete success', type: 'success' })
    }
  }
}
</script>

