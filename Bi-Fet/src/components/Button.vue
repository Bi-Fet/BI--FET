<template>
    <button class="btn btn-primary" @click="handleClick">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: 'ButtonComponent',
    props: {
        text: {
            type: String,
            required: true
        },
        targetId: {
            type: String,
            required: true
        }
    },
    emits: ['buttonClick'],
    methods: {
        handleClick() {
            this.$emit('buttonClick', this.targetId);
        }
    }
};
</script>

<style scoped>
.btn {
    border: 1px solid var(--text-secondary-color);
    border-radius: 50px;
    padding: 1rem 2rem;
    font-family: var(--font-family-sans-serif);
    font-size: var(--font-size-base);
    font-weight: var(--font-weight-bold);
    color: var(--text-secondary-color);
    cursor: pointer
}
</style>