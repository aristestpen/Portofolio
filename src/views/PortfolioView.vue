<script>
export default {
  data() {
    return {
      activeTab: 1,
      items: [
        {
          id: 1,
          name: 'Komship',
          imageUrl: 'komship',
          status: 'Komship is a delivery service platform to help you send packages both COD and Non-COD without minimum delivery.',
          tech: 'Android Development',
          github: 'null',
          demo: 'https://play.google.com/store/apps/details?id=com.komerce.komshipmobile'
        },
        {
          id: 2,
          name: 'UI Mobile',
          imageUrl: 'ui-akost',
          status: 'UI Mobile Apps design for accommodation booking platform with modern and user-friendly interface.',
          tech: 'Figma',
          github: 'null',
          demo: 'null'
        },
        {
          id: 3,
          name: 'Web Aher Store',
          imageUrl: 'madu-full',
          status: 'This website provides comprehensive information about BJ honey, covering health benefits and production processes.',
          tech: 'Bootstrap',
          github: 'null',
          demo: 'null'
        },
        {
          id: 4,
          name: 'Komtim',
          imageUrl: 'komtim',
          status: 'Komtim simplifies finding and hiring experienced talents to help manage your business efficiently and effectively.',
          tech: 'Mobile Development',
          github: 'null',
          demo: 'https://play.google.com/store/apps/details?id=id.android.kmpartner.production'
        },
        {
          id: 5,
          name: 'Mitra Komtim',
          imageUrl: 'mitra-komtim',
          status: 'Mitra Komtim is an Indonesian Human Resource Information System (HRIS) designed to simplify HR processes efficiently.',
          tech: 'Mobile Development',
          github: 'null',
          demo: 'https://play.google.com/store/apps/details?id=id.komerce.mitrakomtim&hl=id'
        }
      ]
    };
  }
}
</script>
<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <!-- <div class="h-[1px] w-10 bg-amber-200 md:w-20 aos-init aos-animate"></div> -->
          <h4>Past Project Experience</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300">
            Explore the projects I've worked on so far</h4>
        </div>
      </header>
      <section>
        <div>
          <div class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-3 md:gap-3 xl:grid-cols-3 xl:gap-3 2xl:gap-5 fade-zoom-in">
            <div v-for="item in items" :key="item.id">
              <div
                class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-amber-50 md:gap-3 px-5 py-5 lg:px-5 h-full">
                <div class="flex items-center justify-center p-0 w-full h-48 lg:p-0 zoom-in">
                  <img alt="Portfolio" loading="lazy" decoding="async" data-nimg="1" class="portfolio-image drop-shadow-xl rounded rounded-xl w-full h-full object-cover"
                    :src="'/img/portfolio-' + item.imageUrl + '.png'">
                </div>
                <div class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg">
                  <div class="title-text font-medium text-secondary">{{ item.name }}
                  </div>
                  <div class="w-full text-left text-[10px] text-[#c1c1c1] md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                  <div class="w-full mt-4 text-normal text-sm text-left text-amber-200">
                    {{ item.tech }}
                  </div>
                  <div class="w-full flex justify-end">
                    <div class="flex cursor-pointer items-end gap-2 text-primary">
                      <a v-if="item.github !== 'null'"
                        :href="item.github" target="_blank" rel="noreferrer"
                        title="View github repository" class="transition-all hover:text-accent">
                        <svg stroke="currentColor"
                          fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"
                          height="16" width="16" xmlns="http://www.w3.org/2000/svg">
                          <path
                            d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22">
                          </path>
                        </svg></a>
                        <a v-if="item.demo !== 'null'" :href="item.demo" target="_blank" rel="noreferrer"
                        title="View finished project" class="transition-all hover:text-accent">
                        <svg stroke="currentColor"
                          fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"
                          height="18" width="18" xmlns="http://www.w3.org/2000/svg">
                          <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                          <polyline points="15 3 21 3 21 9"></polyline>
                        <line x1="10" y1="14" x2="21" y2="3"></line>
                      </svg></a></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </article>
</div></template>

<style>
.item-card {
  min-height: 220px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.portfolio-image {
  height: 180px;
  width: 100%;
  object-fit: cover;
  object-position: center;
}
.item-card:hover {
  transition: transform 0.3s ease;
  transform: translateY(-8px);
}
svg:hover{
  stroke: #ffdb70;
}
@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

/* Menggunakan animasi pada elemen yang diinginkan */
.fade-zoom-in {
  animation: fadeZoomIn 1s ease-in-out;
}
</style>