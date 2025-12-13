<script>
import '@mdui/icons/close.js';

export default {
    name: 'MapOverlay',
    props: {
        width: {
            type: Number,
            required: true
        },
        height: {
            type: Number,
            required: true
        },
        XYitems: {
            type: Array,
            default: () => []
        }
    },
    data() {
        return {
            selectedItem: null
        }
    },
    methods: {
        MarkerClick(item) {
            this.selectedItem = item;
        },
        CloseDetail() {
            this.selectedItem = null;
        }
    }
};
</script>

<template>
    <div class="map-overlay" :style="{ width: width + 'px', height: height + 'px' }">
        <div v-for="item in XYitems" :key="item.id">
            <button class="map-marker" @click="MarkerClick(item)"
                :style="{ left: item.baseInfo.originalX + 'px', top: item.baseInfo.originalY + 'px' }"
                :title="`(${Math.round(item.baseInfo.originalX)}, ${Math.round(item.baseInfo.originalY)}) ${$t(item.baseInfo.name)}\n${$t(item.baseInfo.desc)}`">
                <img class="marker-icon" v-if="item.baseInfo.icon !== 'null'" :src="'/image/icon/' + item.baseInfo.icon" alt="Marker Icon" />
                <div v-else style="font-size: 26px;color: #ffffff;text-shadow: 0 0 8px #000000;text-align: center;font-weight: bold;">{{ $t(item.baseInfo.name) }}</div>
            </button>
        </div>

        <Teleport to="body">
            <div class="map-marker-text animate__animated animate__fadeInRight" v-if="selectedItem">
                <div class="map-marker-text-navbar">
                    <div></div>
                    <button class="map-marker-text-navbar-close"
                        @click="CloseDetail"><mdui-icon-close></mdui-icon-close></button>
                </div>
                <div class="map-marker-text-name">{{ $t(selectedItem.baseInfo.name) }}</div>
                <div class="map-marker-text-desc">{{ $t(selectedItem.baseInfo.desc) }}</div>
            </div>
        </Teleport>
    </div>
</template>

<style scoped>
.map-marker-text-navbar {
    display: flex;
    justify-content: space-between;
    gap: 8px;
    align-items: center;
    margin-bottom: 10px;
}

.map-marker-text-navbar-title {
    font-weight: bold;
}

.map-marker-text-navbar-close {
    background: none;
    border: none;
    cursor: pointer;
    font-size: 20px;
    color: #ffffff;
    background-color: var(--theme-color);
    padding: 4px;
    border-radius: var(--border-radius);
    display: flex;
    align-items: center;
    justify-content: center;
    transition: opacity 0.3s;

    &:hover {
        opacity: 0.8;
    }
}

.map-marker-text-name {
    text-align: center;
    background-color: var(--background-color);
    padding: 0 8px;
    margin-bottom: 8px;
    border-radius: var(--border-radius);
    color: var(--theme-color);
    font-weight: bold;
    font-size: 20px;
}

.map-marker-text-desc {
    font-size: 16px;
}

.map-marker-text {
    z-index: 9999;
    position: fixed;
    top: 60px;
    right: 16px;
    background-color: var(--background-color-oc);
    backdrop-filter: blur(10px);
    border: 4px solid var(--theme-color);
    border-radius: var(--border-radius);
    padding: 10px;
    max-width: 200px;
    overflow: hidden;
    word-wrap: break-word;
}

.map-overlay {
    position: absolute;
    top: 0;
    left: 0;
    pointer-events: none;
    /* Allow clicks to pass through to map for dragging */
    z-index: 10;
}

.map-marker {
    position: absolute;
    transform: translate(-50%, -50%);
    /* Center marker on coordinate */
    display: flex;
    flex-direction: column;
    align-items: center;
    pointer-events: auto;
    border: none;
    background: transparent;
    /* Re-enable clicks for markers */
    cursor: pointer;
}

.marker-icon {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
}
</style>
