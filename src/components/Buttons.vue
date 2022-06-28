<script setup>
    defineProps({
        variant: String,
        disableShadow: Boolean,
        disabled: Boolean,
        startIcon: String,
        endIcon: String,
        size: String,
        color: String
    })
</script>

<template>
    <button 
        :class="[
            {'noShadow': disableShadow},
            variant == 'outline' ? 'outline' : '',
            variant == 'text' ? 'text' : '',
            size == 'sm' ? 'sm-btn' : '',
            size == 'md' ? 'md-btn' : '',
            size == 'lg' ? 'lg-btn' : '',
            color == 'default' ? 'default' :'',
            color == 'primary' ? 'primary' :'',
            color == 'secondary' ? 'secondary' :'',
            color == 'danger' ? 'danger' :'',
        ]"
        :disabled="disabled ? true : false"
    >
       <span v-if="startIcon" class="material-icons-outlined">{{ startIcon }}</span>
       Default
       <span v-if="endIcon" class="material-icons-outlined">{{ endIcon }}</span>
    </button>
</template>

<style scoped>
button {
    display: flex;
    align-items: center;
    column-gap: 10px;
    font-family: var(--ff-poppins);
    font-size: 14px;
    font-weight: 500;
    padding: 8px 16px;
    margin: 20px 0;
    text-align: center;
    color: var(--color-gray-1);
    background-color: var(--color-gray-5);
    border: none;
    box-shadow: 0px 2px 3px rgba(51, 51, 51, 0.2);
    border-radius: 6px;
    cursor: pointer;
}
button:is(:hover, :focus),
button.default:is(:hover, :focus) {
    background-color: var(--color-gray-3);
}

button.outline {
    border: 1px solid var(--color-primary-1);
    background-color: var(--color-white);
    color: var(--color-primary-1);
    box-shadow: none;
}

button.text {
    background-color: var(--color-white);
    color: var(--color-primary-1);
    box-shadow: none;
}
button.outline:is(:hover, :focus), 
button.text:is(:hover, :focus) {
    background-color: var(--color-primary-3);
}

button.noShadow {
    box-shadow: none;
}

button:disabled {
    background-color: var(--color-gray-5);
    color: var(--color-gray-4);
    cursor: not-allowed;
}
button.text:disabled {
    background-color: transparent;
    color: var(--color-gray-4);
}

.material-icons-outlined {
    font-size: 14px;
}

button.sm-btn {
    padding: 6px 12px;
}
button.md-btn {
    padding: 8px 16px;
}
button.lg-btn {
    padding: 11px 22px;
}

button.default {
    color: var(--color-gray-1);
    background-color: var(--color-gray-5);
}
button.primary {
    color: var(--color-white);
    background-color: var(--color-primary-1);
}
button.primary:is(:hover, :focus) {
    background-color: var(--color-primary-2);
}
button.secondary {
    color: var(--color-white);
    background-color: var(--color-secondary-1);
}
button.secondary:is(:hover, :focus) {
    background-color: var(--color-secondary-2);
}
button.danger {
    color: var(--color-white);
    background-color: var(--color-danger-1);
}
button.danger:is(:hover, :focus) {
    background-color: var(--color-danger-2);
}

</style>