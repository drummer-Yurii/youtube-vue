<template>
    <a class="mb-7 group">
        <VideoItemThumbnail :index="index" />
        <VideoItemInfo :index="index" />
    </a>
</template>

<script>
import VideoItemInfo from './VideoItemInfo.vue';
import VideoItemThumbnail from './VideoItemThumbnail.vue';

export default {
    components: {
        VideoItemThumbnail,
        VideoItemInfo
    },
    props: ['index']
}
</script>