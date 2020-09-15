<template>
  <div>
    <d-navbar
      :routes="routes"
      :app-title="appTitle"
      elevate-on-scroll
      right
    />
    <Nuxt />
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tenetur, corrupti.</p>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ducimus, hic nemo, non, cum ullam veritatis architecto dolorem velit adipisci eligendi nisi expedita facere temporibus quibusdam veniam iste ad. Ipsum error quis recusandae, eveniet minus quam necessitatibus libero ex harum accusamus aut, voluptate mollitia, reiciendis eos vero porro assumenda. Ratione, praesentium!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus impedit ab nisi nemo asperiores quam commodi, eaque deserunt tempora dolor.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque veritatis ea aliquam magnam natus ipsum quaerat ut corporis odit! Cumque illum provident mollitia labore, fugiat doloribus facere quis error odio repellat nisi fuga eligendi laborum quibusdam ad! Quasi maxime, laborum labore facilis, nobis at debitis incidunt omnis, nemo sed suscipit.</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minus iste natus ratione exercitationem impedit neque, nostrum cupiditate dolor delectus, quia aliquam facere commodi vitae recusandae laboriosam provident voluptas nesciunt dicta. Necessitatibus numquam magnam a porro fugit earum repellat voluptatibus quos odio impedit, consectetur ipsum deserunt iure nemo quam similique esse odit! Eos fuga maiores eius vel recusandae quod aliquid nihil obcaecati autem, voluptatibus quibusdam odit a tenetur reprehenderit, ea porro hic, aliquam architecto! Quam eaque dignissimos ratione reiciendis dolorem pariatur aspernatur repellendus! A quod eligendi dignissimos optio dolorem, enim reiciendis ea incidunt laudantium numquam ratione atque perferendis natus, temporibus maxime?</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minus iste natus ratione exercitationem impedit neque, nostrum cupiditate dolor delectus, quia aliquam facere commodi vitae recusandae laboriosam provident voluptas nesciunt dicta. Necessitatibus numquam magnam a porro fugit earum repellat voluptatibus quos odio impedit, consectetur ipsum deserunt iure nemo quam similique esse odit! Eos fuga maiores eius vel recusandae quod aliquid nihil obcaecati autem, voluptatibus quibusdam odit a tenetur reprehenderit, ea porro hic, aliquam architecto! Quam eaque dignissimos ratione reiciendis dolorem pariatur aspernatur repellendus! A quod eligendi dignissimos optio dolorem, enim reiciendis ea incidunt laudantium numquam ratione atque perferendis natus, temporibus maxime?</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minus iste natus ratione exercitationem impedit neque, nostrum cupiditate dolor delectus, quia aliquam facere commodi vitae recusandae laboriosam provident voluptas nesciunt dicta. Necessitatibus numquam magnam a porro fugit earum repellat voluptatibus quos odio impedit, consectetur ipsum deserunt iure nemo quam similique esse odit! Eos fuga maiores eius vel recusandae quod aliquid nihil obcaecati autem, voluptatibus quibusdam odit a tenetur reprehenderit, ea porro hic, aliquam architecto! Quam eaque dignissimos ratione reiciendis dolorem pariatur aspernatur repellendus! A quod eligendi dignissimos optio dolorem, enim reiciendis ea incidunt laudantium numquam ratione atque perferendis natus, temporibus maxime?</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      appTitle: 'Nuxt/Vue Components',
      routes: [
        { title: 'Home', path: '/' },
        { title: 'About', path: '/about' },
        { title: 'Contact', path: '/contact' }
      ],
      isSidebarOpen: true
    }
  }
}
</script>

<style lang="scss">
body {
  @include theme-aware('background', 'bg-main');
  @include theme-aware('color', 'text-main');
}

body.no-scroll {
  overflow: hidden;
}
</style>>
