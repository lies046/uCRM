<script setup xmlns="http://www.w3.org/1999/html">
import {Link } from "@inertiajs/inertia-vue3";
import { ref } from 'vue';

const newTitle = ref('')
const newContent = ref('')
</script>

<template>
    Inertiaテストです。<br>
    <a href="/">あタグ経由です。</a><br>
    <Link href="/">Link経由です</Link><br>
    <Link :href="route('inertia.index')">名前付きルートの確認です</Link>
    <br>
    <Link :href="route('inertia.show', {id: 50})">ルートパラメーターのテストです</Link>

    <div class="mb-8"></div>
    <input type="text" name="newTitle" v-model="newTitle">{{ newTitle }}<br>
    <input type="text" name="newContent" v-model="newContent">{{ newContent }}<br>
    <Link as="button" method="post" :href="route('inertia.store')" :data="{title: newTitle, content: newContent}">DB保存テスト</Link>
</template>
