<script setup>
const myModel = ref(null)
const newUrl = ref('')
</script>
<template>
    <div>
        <button class="btn" @click="myModel.showModal()">自定义</button>
        <dialog ref="myModel" class="modal">
            <div class="modal-box">
                <h3 class="font-bold text-lg">设置其他网页</h3>
                <textarea v-model="newUrl" class="textarea textarea-bordered h-24 w-full" placeholder="举例：https://wubug.cn"></textarea>
                <div class="modal-action">
                    <form method="dialog">
                        <!-- if there is a button in form, it will close the modal -->
                        <button class="btn" @click="$emit('changeurl',newUrl)">设置</button>
                    </form>
                    <form method="dialog" class="modal-backdrop">
    <button>close</button>
  </form>
                </div>
            </div>
        </dialog>
    </div>
</template>