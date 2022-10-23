<template>
    <div>
        <div class="card-body">
            <h5 class="card-title">{{post.title}}</h5>
            <p class="card-text">{{post.content}}</p>
            <p class="card-text">Category: {{post.category ? post.category.name : '-'}}</p>
            <p class="card-text">
                Tag: <span v-if="post.tags.length == 0">-</span>
                <span v-else v-for="(tag, tagIndex) in post.tags" :key="tagIndex">{{tag.name + '; '}}</span>
            </p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SinglePost',
    props: {
        post: Object
    }
}
</script>

<style scoped lang="scss">

</style>