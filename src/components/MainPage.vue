<template>
    <div class="about-page">
        <div class="holder-container">
            <AntRow align="top" :gutter="16">
                <AntCol :lg="isMobile ? 24 : isTablet ? 24 : 6" :xs="24" :md="24">
                    <div class="portrait-container">
                        <div class="portrait-wrapper" :style="{
                       paddingBottom: isMobile || isTablet ? '20px' : '0px'
                    }" >
                            <img :src="portraitImage" alt="Portrait" title="Not a picture of me but I do have a moustache"
                                class="portrait-image" :style="{
                                    marginTop: isMobile || isTablet ? '120px' : '140px',
                                    width: isMobile || isTablet ? '72%' : '90%',
                                    marginLeft: isMobile || isTablet ? '0px' : '34px'
                                }" />
                        </div>
                    </div>
                </AntCol>
                <AntCol :xs="24" :lg="isMobile ? 24 : isTablet ? 24 : 18">
                    <h1 class="page-header" :style="{
                        color: '#FFF',
                        paddingTop: isMobile || isTablet ? '10px' : '82px',
                        fontWeight: '450',
                        textAlign: 'center',
                        marginLeft: isMobile || isTablet ? '0px' : '0px'
                    }">
                        About Me!
                    </h1>
                    <div class="bio-formatting">
                        <p class="bio-text-formatting">
                            This is a test page to experiment with Vue.js and Ant Design to make a simple responsive page. I am a Full-Stack Web Developer (MERN) with
                            a passion for learning new technologies and solving problems. I have another project that used
                            Ant Design (within React) called Recall Rumble! It was the final project in my coding bootcamp that I was lucky
                            enough to lead! It is a cool concentration-like card game where the player matches cards for a
                            score. The fewer turns it takes, the better! You can checkout it out on my portfolio linked in the footer.
                        </p>
                        <p class="bio-text-formatting">
                            Here is some placeholder text to experiment with Ant Design within Vue as it has some differences from the React version, here I am using a  &lt;p&gt;&lt;/p&gt; tag. Below this I will use the Ant Design Typography component.
                        </p>
                        <Typography class="bio-text-formatting">
                                This block of text is using the Ant Design &lt;Typography&gt; component.
                                I am using it in place of the Ant Design Paragaph tag as it seems like Ant Design for Vue is a little different from the React version.
                                The Paragraph tag doesn't seem to exist within the Vue version.
                        </Typography>
                        <Typography class="bio-text-formatting">
                                The Ant Design Typography component seems to have some quirks as well, it is registered as an &lt;article&gt;&lt;/article&gt; so I need to designate article styling for it to look the same as the standard &lt;p&gt;&lt;/p&gt; tags used above. That seems a little counter-intuitive to me but I am sure there is a reason for it, just complicates styling a little bit.
                        </Typography>
                        <Typography class="bio-text-formatting">
                                I have also added the React version I made of this simple about me page to the footer below. I wanted to explore making the same app within React and Vue for fun! It was also to experiment with deploying to AWS (Amplify).
                        </Typography>
                    </div>
                </AntCol>
            </AntRow>
        </div>
    </div>
</template>
  
<script>
import { Row as AntRow, Col as AntCol, Typography } from 'ant-design-vue';
import portraitImage from '@/assets/logo512.webp';

export default {
    name: 'MainPage',
    components: {
        AntRow,
        AntCol,
        Typography
    },
    data() {
        return {
            isMobile: false,
            isTablet: false,
            portraitImage
        };
    },
    mounted() {
        this.handleScreenSize();
        window.addEventListener('resize', this.handleScreenSize);
    },
    beforeUnmount() {
        window.removeEventListener('resize', this.handleScreenSize);
    },
    methods: {
        handleScreenSize() {
            this.isMobile = window.innerWidth < 768;
            this.isTablet = window.innerWidth >= 768 && window.innerWidth < 992;
        }
    }
};
</script>
  
<style src="../styles/global.css"></style>
  