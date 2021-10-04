<template>
    <div>
        <button @click="$emit('btn-click')" :style="{background: color}" class="btn">{{ text }}</button>
    </div>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String
    },
    emits: ['btn-click']
}
</script>