<template>
<!-- This example requires Tailwind CSS v2.0+ -->
<div class="bg-gray-50">
  <div class="relative overflow-hidden">
    <div class="absolute inset-y-0 h-full w-full" aria-hidden="true">
      <div class="relative h-full">
        <svg class="absolute right-full transform translate-y-1/3 translate-x-1/4 md:translate-y-1/2 sm:translate-x-1/2 lg:translate-x-full" width="404" height="784" fill="none" viewBox="0 0 404 784">
          <defs>
            <pattern id="e229dbec-10e9-49ee-8ec3-0286ca089edf" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="784" fill="url(#e229dbec-10e9-49ee-8ec3-0286ca089edf)" />
        </svg>
        <svg class="absolute left-full transform -translate-y-3/4 -translate-x-1/4 sm:-translate-x-1/2 md:-translate-y-1/2 lg:-translate-x-3/4" width="404" height="784" fill="none" viewBox="0 0 404 784">
          <defs>
            <pattern id="d2a68204-c383-44b1-b99f-42ccff4e5365" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="784" fill="url(#d2a68204-c383-44b1-b99f-42ccff4e5365)" />
        </svg>
      </div>
    </div>

    <div class="relative pt-6 pb-16 sm:pb-24">

      <div class="mt-16 mx-auto max-w-7xl px-4 sm:mt-24 sm:px-6">
        <div class="text-center">
          <h1 class="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl">
            <span class="block">Lazy loading images with a </span>
            <span class="block text-indigo-600">low quality placeholder</span>
          </h1>
          <p class="mt-3 max-w-md mx-auto text-base text-gray-500 sm:text-lg md:mt-5 md:text-xl md:max-w-3xl">
            The images below will lazy load using low quality placeholders before they fully render the HD version
          </p>
        </div>
      </div>
    </div>

    <div>
      <div class="max-w-2xl mx-auto py-16 px-4 sm:py-24 sm:px-6 lg:max-w-7xl lg:px-8">

        <div class="mt-6 grid grid-cols-1 gap-y-10 gap-x-6 sm:grid-cols-2 lg:grid-cols-3 xl:gap-x-6">
          
          <div v-for="image in images" :key="image.public_id" class="group relative">
            <div class="w-full min-h-80 bg-gray-200 aspect-w-1 aspect-h-1 rounded-md overflow-hidden group-hover:opacity-75 lg:h-80 lg:aspect-none">
              <cld-image 
                :public-id="image.public_id" 
                alt="credit" 
                class="w-full h-full object-center object-cover lg:w-full lg:h-full"
              />
            </div>
            <div class="mt-4 text-center">
                <h3 class="text-sm text-gray-700" v-html="image.credit"></h3>
            </div>
            </div>
          </div>

        </div>
      </div>
    </div>

  </div>
</div>

</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return {
      images: [
    {
      public_id:'nuxtjs-low-quality-placeholder/ryan-ancill-aJYO8JmVodY-unsplash.jpg',
      credit: 'Photo by <a href="https://unsplash.com/@ryanancill?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Ryan Ancill</a> on <a href="https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>',
    },
    {
      public_id:'nuxtjs-low-quality-placeholder/ali-karimiboroujeni-XAwyrABB2IA-unsplash.jpg',
      credit:'Photo by <a href="https://unsplash.com/@alikarimi_photography?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Ali Karimiboroujeni</a> on <a href="https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>',
    },
    {
      public_id:'nuxtjs-low-quality-placeholder/nathan-dumlao-f5DHtik4hWc-unsplash.jpg',
      credit:'Photo by <a href="https://unsplash.com/@nate_dumlao?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Nathan Dumlao</a> on <a href="https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>',
    },
    {
      public_id:'nuxtjs-low-quality-placeholder/pawel-czerwinski-DKzsQT9zUPk-unsplash.jpg',
      credit:'Photo by <a href="https://unsplash.com/@pawel_czerwinski?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Pawel Czerwinski</a> on <a href="https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>',
    },
    {
      public_id:'nuxtjs-low-quality-placeholder/toa-heftiba-FV3GConVSss-unsplash.jpg',
      credit:'Photo by <a href="https://unsplash.com/@heftiba?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Toa Heftiba</a> on <a href="https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>',
    },
    {
      public_id:'nuxtjs-low-quality-placeholder/elise-wilcox-Q6GRqKGuswc-unsplash.jpg',
      credit:'Photo by <a href="https://unsplash.com/@elise_outside?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Elise Wilcox</a> on <a href="https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>'
    }
  ]
    };
  }
}
</script>
