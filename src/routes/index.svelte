<script>

  import { Pagination } from "swiper";
  import { Swiper, SwiperSlide } from 'swiper/svelte';
  import 'swiper/scss';
  import 'swiper/scss/pagination';

  let slides = [
    {
      src: 'https://www.fillmurray.com/200/125/',
    },
    {
      src: 'https://www.fillmurray.com/200/125/',
    },
    {
      src: 'https://www.fillmurray.com/200/125/',
    },
  ];

</script>

<h1>Welcome to SvelteKit</h1>

<Swiper
  modules={ [ Pagination ] }
  autoHeight={ true }
  pagination={{ clickable: true }}
>
  {#each slides as slide }
    <SwiperSlide>
      <img src={ slide.src } alt='' />
    </SwiperSlide>
  {/each}
</Swiper>

