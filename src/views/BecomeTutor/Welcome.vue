<template>
    <section class="become_tutor_welcome">
        <div class="break_down_sec">
            <div class="details">
                <div class="title">Interested in becoming a tutor with Bukassa?</div>
                <div class="sub_title">
                    Earn greater income with more freedom
                </div>
                <div class="list">
                    <div>1. Set your own prices</div>
                    <div>2. Be your own boss</div>
                    <div>3. Work from home, and on your schedule</div>
                </div>
                <div class="apply_btn_wrapper">
                    <ButtonPlainText 
                        buttonText="Apply To Teach" 
                        @buttonAction="gotoapplication()"
                    />
                </div>
            </div>
            <div class="image_wrapper">
                <img src="../../assets/sec2.png">
            </div>
        </div>
    </section>
</template>

<script>
import ButtonPlainText from "@/components/buttons/ButtonPlainText.vue";

export default {
    components: { ButtonPlainText },
    methods: {
        gotoapplication() {
            this.$router.push('/become-tutor/application');
        }
    }
}
</script>

<style scoped>
    .become_tutor_welcome {
        
    }
    .break_down_sec {
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 80vh;
        width: 90%;
        margin: 5% auto;
    }
    .break_down_sec > div {
        height: 90%;
    }

    .details {
        width: 40%;
        margin-left: 5%;
    }
    .details .title {
        font-size: 240%;
        font-weight: 700;
        color: var(--burgundy-200);
    }
    .details .sub_title {
        font-size: 150%;
        font-weight: 600;
        color: var(--paper-grey-600);
        margin: 6% 0;
    }
    .list {
        line-height: 150%;
        margin: 5% 0;
    }
    .list > div {
        padding: none;
        margin: 2% 0;
        font-size: 120%;
        color: var(--paper-grey-800);
        font-weight: 600;
    }

    .apply_btn_wrapper {
        width: 30%;
        height: 50px;
    }
    .apply_btn_wrapper button {
        border: 2px solid var(--burgundy-200);
        background: #ee9d9d1c;
        color: var(--burgundy-200);
        border-radius: 5px;
    }

    .break_down_sec .image_wrapper {
        width: 35%;
        border-radius: 40px 0 40px 0;
        overflow: hidden;
        margin-right: 5%;
    }
    .break_down_sec .image_wrapper img {
        object-fit: cover;
    }
</style>