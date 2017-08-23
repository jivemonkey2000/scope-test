<template>
    <div>
        <slot :prop-name="data">

        </slot>
    </div>
</template>

<script>
    export default {
        name: 'bComponent',

        props: ['data']
    }
</script>