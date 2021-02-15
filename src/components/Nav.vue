<template>
    <nav>
        <div class="mx-auto">
            <h1><strong>Vue</strong> simple Chat App </h1>
            <div v-if="isLogin" class="login">
                <div class="text-green-300 mr-2">{{ user.displayName.split(' ')[0] }}</div>
                <Avatar :src="user.photoURL" />
                <button class="text-gray-400 hover:text-white" @click="signOut">
                Sign Out
                </button>
            </div>
            <button v-else class="text-green-500 hover:text-green-600" @click="signIn">
                Sign In
            </button>
        </div>
    </nav>
</template>

<script>
import Avatar from './Avatar.vue'
import { useAuth } from '@/firebase'

export default {
    components: { Avatar },
    setup() {
        const { user, isLogin, signIn, signOut} = useAuth()
        return { user, isLogin, signIn, signOut }
    }
}
</script>