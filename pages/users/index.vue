<template>
    <div> 
        <h1 class="title">Nuxt as API server</h1>
        <h2 class="subtitle">Users</h2>
        <button type="button" @click="$fetch">Refresh</button>
        <ol>
            <li
                v-for="user in users"
                :key="user.id"
                :class="{'highlight': user.highlight}"
                @click="getUserInfo(user.id)"
            >{{ user.full_name }}</li>
        </ol>
        <div v-if="userInfo">
            <hr>
            <h3>{{ userInfo.first_name }} {{ userInfo.last_name }}</h3>
            <div>Email: {{ userInfo.email }}</div>
            <img :src="userInfo.avatar" alt="avatar">
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            users: [],
            userInfo: null
        }
    },
    async fetch() {
        try {
            this.users = await this.$axios.$get("/api/users/index");
        } catch (e) {
            console.error(e);
            throw e;
        }
    },
    methods: {
        async getUserInfo(id) {
            try {
                this.userInfo = await this.$axios.$post("/api/users/show", {
                    id
                });
                console.log('userInfo: ', this.userInfo)
            } catch (e) {
                console.error(e);
                throw e;
            }
        }
    }
}
</script>

<style scoped>
li {
    cursor: pointer;
}
.highlight {
    color: green;
    font-weight: bold;
}
</style>