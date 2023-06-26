<template>
    <footer class="footer">
        <div class="footer-bar">
            <Space size="large" align="center">
                <a href="https://github.com/DomenicoBarb" target="_blank" rel="noopener noreferrer">
                    <img src="../assets/white-github.png" alt="Github" class="logo" title="My GitHub profile" />
                </a>
                <a href="https://www.linkedin.com/in/domenico-a-barberi/" target="_blank" rel="noopener noreferrer">
                    <img src="../assets/white-linked-in.png" alt="LinkedIn" class="logo" title="My LinkedIn profile" />
                </a>
            </Space>
        </div>
    </footer>
</template>
  
<script>
import { Space } from 'ant-design-vue';

export default {
    name: 'PageFooter',
    components: {
        Space
    }
};
</script>

<style src="../styles/global.css"></style>