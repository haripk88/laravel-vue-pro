<template>
    <div class="auth-container">
        <h1>Login</h1>
        <input type="email" v-model="email" placeholder="Enter your email address" name="email" id="email">
        <input type="password" v-model="password" placeholder="Enter your password" name="password" id="password">
        <button @click="handleLogin" :disabled="loading">
            {{ loading ? 'Logging in...' : 'Login' }}
        </button>

        <p>Don't have an account? <router-link to="/register">Register here</router-link></p>
    </div>
</template>
<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';
</script>