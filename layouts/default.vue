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
      ]
    }
  }
}
</script>

<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
