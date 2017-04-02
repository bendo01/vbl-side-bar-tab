<template>
    <div class="tab-pane" :class="{ 'is-active':isActive }">
        <slot></slot>
    </div>
</template>

<script>
'use strict';
export default {
    props: {
        icon: { required: true },
        name: { required: true },
        selected: { default: false }
    },

    data () {
        return {
            isActive: false,
            iconData: this.icon
        };
    },
    mounted () {
        this.isActive = this.selected;
    }
};
</script>
<style lang="scss">
    .tab-pane {
        height: 95vh;
    }
</style>
