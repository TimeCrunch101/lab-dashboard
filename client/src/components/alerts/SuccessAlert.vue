<script setup>
const props = defineProps({
    successMessage: String
})

const dismissAlert = () => {
    const alertDiv = document.getElementById("success1")
    alertDiv.classList.add('hidden')
    location.reload();
}



</script>

<template>
    <div id="success1" class="alert alert-success">
        <!-- <p>This is a <span class="warning">warning</span> alert</p> -->
        <p>{{successMessage}}</p>
        <div @click="dismissAlert" class="alert-action">
            <i class="fa-solid fa-xmark fa-lg"></i>
        </div>
    </div>
</template>

<style scoped>
.alert {
    position: absolute;
    top: 10px;
    left: 50%;
}
.alert-action:hover {
    cursor: pointer;
}

.hidden {
    display: none;
}

</style>