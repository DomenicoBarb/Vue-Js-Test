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
                <a href="https://domenico-barberi-react-portfolio.netlify.app/" target="_blank" rel="noopener noreferrer">
                    <img src="../assets/logo512.webp" alt="ReactPortfolio" class="portfoliologo" title="React Portfolio" />
                </a>
                <a href="https://dev.d3cbjkk0ofnz30.amplifyapp.com/" target="_blank" rel="noopener noreferrer">
                    <img src="../assets/react.png" alt="ReactVersion" class="logo" title="About Me React Version" />
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