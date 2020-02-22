<template>
    <div class="bucket-item">
        {{item.task}}
        {{item.message}}
        {{item.status}}
        {{item.date}}
    </div>
</template>

<script>
    export default {
        name: 'BucketItem',
        props: {
            item: String
        }
    }
</script>
