<template>
    <div>
        <h2>This is a popup</h2>
        <button @click="$emit('close', 'Marcel')">Close</button>
    </div>
</template>

<script>
    export default {
        name: "Popup",
        emits: ["close"],
    }
</script>