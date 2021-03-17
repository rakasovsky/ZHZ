<template>
  
   <client-only>
       <div class="m25 g_wrapper">
             <LightGallery 
            :images="images"
            :index="index"
            :disable-scroll="true"
            @close="index = null"
        />
        <div class="seo">
          <h1>Фотографии постояльцев зооотеля Забота</h1>
           <h2>Галерея животных</h2>
        </div>
        <h2 class="fs42" >Фотографии наших постояльцев</h2>
        <ul>
            <!-- Thumbnails -->
            <li
            v-for="(image, imageIndex) in [
                '/1.jpg',
                '/g/zoootel (6).jpg',
                '/g/zoootel (7).jpg',
                '/g/zoootel (12).jpg',
                '/g/zoootel (13).jpg',
                '/g/zoootel (17).jpg',
                '/g/zoootel (18).jpg',
                '/g/zoootel (19).jpg',
                '/g/zoootel (20).jpg',
                '/g/v1.jpg',
                '/g/v2.jpg',
                
            ]"
            :key="imageIndex"
            class="thumb"
            @click="index = imageIndex"
            >
            <img :src="image">
            </li>
        </ul>
       </div>
</client-only> 
</template>
<script>
export default {
    head: {
        title: 'Галерея Зооотеля Забота | Харьков',
        meta: [
        {
            hid: 'description',
            name: 'description',
            content: 'Фотографии Зооотель Забота | Харьков | Отель для животных Харьков | Гостиница для собак Харьков | Передержка собак Харьков | Отель Забота Харьков'
        },
        {
            hid: 'keywords',
            name: 'keywords',
            content: 'Зооотель, Зоо гостиница, Передержка, Гостиница для животных, Отель Забота, Фотогалерея, Фотографии'
        }
        ],
 
    },
    data: function () {
      return {
        images: [
          {
            title: 'Big vulture flying',
            url: '/1.jpg',
          },
          {
            title: 'Frog soak on water',
            url: '/g/zoootel (6).jpg',
          },
          {
            title: 'Fawn in warm autumn sun',
               url: '/g/zoootel (7).jpg',
          },
          {
            title: 'Mountain goat on the rocks',
            url: '/g/zoootel (12).jpg',
          },
          {
            title: 'Mountain goat on the rocks',
            url: '/g/zoootel (13).jpg',
          },
          {
            title: 'Mountain goat on the rocks',
            url: '/g/zoootel (17).jpg',
          },
          {
            title: 'Mountain goat on the rocks',
            url: '/g/zoootel (18).jpg',
          },
          {
            title: 'Mountain goat on the rocks',
            url: '/g/zoootel (19).jpg',
          },
          {
            title: 'Mountain goat on the rocks',
            url: '/g/zoootel (20).jpg',
          },
          {
            title: 'Mountain goat on the rocks',
            url: '/g/zoootel (4).jpg',
          },
          {
            title: 'Mountain goat on the rocks',
            url: '/g/zoootel (8).jpg',
          },
        ],
        index: null
      };
    },
}
</script>

<style lang="scss" scoped>
  .g_wrapper {
    padding: 100px 0;
    h2 {
      text-align: center;
    }
  }
  ul {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    list-style: none;
    li {
      cursor: pointer;
      width: 200px;
      height: 300px;
      margin: 20px;
      img {
        height: 100%;
        width: 100%;
        object-fit: cover;
      }
    }
  }
</style>