<template>
    <footer>
        <div>Copyright © SAW-MapStats 2025<span v-if="new Date().getFullYear() !== 2025">-{{
            new Date().getFullYear() }}</span>. All rights reserved.</div>
        <div>Email: <a href="mailto:example@example.com">example@example.com</a></div>
    </footer>
</template>

<style>
footer {
    position: fixed;
    bottom: 0;
    left: 0;
    z-index: 9999;
    width: 100%;
    padding: 10px;
    background-color: var(--background-color);
    backdrop-filter: blur(10px);
    font-size: 14px;
    color: #8a8a8a;
    text-align: center;
}
</style>