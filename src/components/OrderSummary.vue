<script setup>
import {ref} from 'vue'

defineProps({
    msg: String,
})

</script>

<template>
    <div class="order-summary">
        <img src="../assets/images/illustration-hero.svg" alt="">
        <div class="order-summary__content">
            <h3 class="order-summary__title">Order Summary</h3>
            <p class="order-summary__description">
                You can now listen to millions of
                songs, audiobooks, and podcasts on
                any device anywhere you like!
            </p>
            <div class="order-summary__plan plan">
                <img src="../assets/images/icon-music.svg" alt="" class="plan__icon">
                <div class="plan__content">
                    <div>
                        <h4>Annual Plan</h4>
                        <span>$59.99/year</span>
                    </div>
                    <a href="#" class="plan__change-link">Change</a>
                </div>
            </div>
            <div class="order-summary__actions actions">
                <button class="primary">Proceed to Payment</button>
                <button class="secondary">Cancel Order</button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

.order-summary {
    display: flex;
    flex-direction: column;
    max-width: 450px;
    border-radius: 20px;
    overflow: hidden;
    background-color: #FFF;

    &__content {
        padding: 42px 48px;
        text-align: center;
    }

    &__title {
        margin-bottom: 10px;
        font-size: 28px;
    }

    &__description {
        margin-bottom: 20px;
    }

    .plan {
        display: flex;
        align-items: center;
        margin-bottom: 30px;
        padding: 25px;
        background-color: hsl(225, 100%, 98%);
        border-radius: 14px;

        &__icon {
            margin-right: 18px;
        }

        &__content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
        }

        &__change-link {
            font-size: 0.875rem;
            font-weight: 700;
            color: hsl(245, 75%, 52%);

            &:hover {
                opacity: .8;
            }
        }
    }

    &__actions {
        display: flex;
        flex-direction: column;
    }
}

button {
    border-radius: 12px;
    border: none;
    padding: 16px;
    font-size: 1em;
    font-weight: 700;
    background-color: transparent;
    color: hsl(224, 23%, 55%);
    cursor: pointer;
    transition: border-color 0.25s;
}

button:not(:last-child) {
    margin-bottom: 16px;
}

button:hover {
    border-color: #646cff;
}

button:focus,
button:focus-visible {
    outline: 4px auto -webkit-focus-ring-color;
}

.primary {
    color: #FFF;
    background-color: hsl(245, 75%, 52%);
    box-shadow:
        rgba(0, 0, 0, 0.1) 0 20px 25px -5px,
        rgba(0, 0, 0, 0.04) 0px 10px 10px -5px;

    &:hover {
        opacity: .8;
    }
}

.secondary {
    &:hover {
        color: hsl(223, 47%, 23%);
    }
}

</style>
