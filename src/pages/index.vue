<template>
	<div class="app">
		  <!--<mce-editor 
    :config           = "Config"
     v-model          = "Value"
    :url              = "Url" //图片上传地址
    :max-size         = "MaxSize"//文件上传最大值
    :accept           = "Accept"//接收什么格式的图片
    :with-credentials = false
    @on-ready         = "onEditorReady"//后面什么的没研究了
    @on-destroy       = "onEditorDestroy"
    @on-upload-success= "onEditorUploadComplete"
    @on-upload-fail   = "onEditorUploadFail"
  ></mce-editor>-->
		
<mceeditor v-model = "Value"></mceeditor>
 Value:{{Value}}
  </div>
</template>

<script>
	import mceeditor from '@/components/mceeditor'
	window.tinymce.baseURL = '/static/tinymce'
	window.tinymce.suffix = '.min'
	export default{
		components: {
			mceeditor
		},
		data(){
			return{
			Value:'',
			}
		}
	}
</script>

<style>
	.app {
		width: 1204px; margin: 0 auto;
	}
</style>