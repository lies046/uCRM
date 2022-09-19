<script setup xmlns="http://www.w3.org/1999/html">
import {Link } from "@inertiajs/inertia-vue3";
</script>

<template>
    Inertiaテストです。<br>
    <a href="/">あタグ経由です。</a><br>
    <Link href="/">Link経由です</Link><br>
    <Link :href="route('inertia.index')">名前付きルートの確認です</Link>
    <br>
    <Link :href="route('inertia.show', {id: 50})">ルートパラメーターのテストです</Link>
</template>
