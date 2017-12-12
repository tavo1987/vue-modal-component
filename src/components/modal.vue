<template>
    <transition
        enter-active-class="animated fadeIn"
        leave-active-class="animated zoomOut">
        <div class="modal" v-if="isActive">
            <div class="modal__content">
                <slot></slot>
            </div>
            <span class="modal__close" @click="close()">
                close
            </span>
        </div>
    </transition>
</template>

<script>
    export default {
        data() {
            return {
                isActive: false
            }
        },
        methods: {
            open() {
                this.isActive = true;
            },
            close() {
                this.isActive = false
            }
        }
    }
</script>

<style lang="scss">
    .modal {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        background: rgba(black, .3);
        z-index: 1000;
        &__content {
            background: white;
            padding:1rem 2rem;
            border-radius:10px;
            max-width: 800px;
            margin-right: 1rem;
            margin-left: 1rem;
        }
        &__close {
            position: absolute;
            right: 1rem;
            top: 1rem;
            background: seagreen;
            padding: .5rem 1rem;
            color: white;
            border-radius: 3px;
        }
    }
</style>

