<template>
    <header>
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <router-link class="navbar-brand" :to="{name: 'home'}">Boolpress</router-link>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item" v-for="(link, linkIndex) in menuLinks" :key="linkIndex">
                        <router-link class="nav-link" :to="{name: link.path}">{{link.name}}</router-link>
                    </li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<script>
    export default {
        name: 'TheHeader',
        data() {
            return {
                menuLinks: [
                    {
                        name: 'Home',
                        path: 'home'
                    },
                    {
                        name: 'Post',
                        path: 'post'
                    },
                    {
                        name: 'Contact',
                        path: 'contact'
                    }
                ]
            }
        }
    }
</script>

<style scoped lang="scss">

</style>