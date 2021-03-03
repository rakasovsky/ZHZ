<template>
    <Gallery :imgs="[{src: 'https://picsum.photos/200/300', thumbnail: 'https://picsum.photos/200/300', w: 200, h: 300, alt: 'random picture from picsum.photos to demonstrate the vue-picture-swipe component', title: 'Some Picture'}, {src: 'https://picsum.photos/200/300', thumbnail: 'https://picsum.photos/200/300', w: 200, h: 300, alt: 'random picture from picsum.photos to demonstrate the vue-picture-swipe component', title: 'Some Picture'}]" />
</template>


<script>
import Gallery from "@/components/Gallery"

export default {
    components: {
        Gallery,
    }
}
</script>