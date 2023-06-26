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
                            This is a test page to experiment with Ant Design and Vue. I am a Full-Stack Web Developer with
                            a passion for learning new technologies and solving problems. I have another project that used
                            Ant Design called Recall Rumble! It was the final project in my coding bootcamp that I was lucky
                            enough to lead! It is a cool concentration-like card game where the player matches cards for a
                            score. The fewer turns it takes, the better! You can checkout it out on my GitHub page linked in the footer.
                        </p>
                        <p class="bio-text-formatting">
                            Here is some placeholder text to see how the page looks with more text, it is using a  &lt;p&gt;&lt;/p&gt; tag. I will use the Ant Design Typography component below this!
                        </p>
                        <Typography class="bio-text-formatting">
                                This is using the Ant Design Typography component. I have to use it as it seems like Ant Design for Vue is a little different from the React version. For example I used the Paragraph component instead of the Typography component in the React equivalent to this.
                        </Typography>
                        <Typography class="bio-text-formatting">
                                The Ant Design Typography component seems to have some quirks as well, it is registered as an &lt;article&gt;&lt;/article&gt; so I need to designate article styling for it to look the same as the standard &lt;p&gt;&lt;/p&gt; tags used above.
                        </Typography>
                        <!-- Rest of the bio-text -->
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
  