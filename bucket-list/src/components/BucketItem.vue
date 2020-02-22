<template>
    <div class="bucket-item">
        <ul>{{item}}}</ul>
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
