<template>
  <div>
    <h1>Consoles</h1>
    <div class="consoles">
      <div v-for="(console, index) in consoles" :key="index" class="console">
        <h3>{{ console.name }}</h3>
        <img :src="console.img" class="console-image" />
        <div class="cost">{{ console.price }}</div>
        <button @click="addItemToCart(console)">Add to cart</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    consoles: [
  {
    name: 'PS5',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fs.yimg.com%2Fos%2Fcreatr-uploaded-images%2F2020-11%2F7c9dc7a0-24f3-11eb-aed4-9f1ba3e2dec3&f=1&nofb=1&ipt=cf9083a68654723698bc2923bfc431a81c3bf4e85a5c5d375560301dd92dcb66&ipo=images",
    price: 399.99
  },
  {
    name: 'Xbox One',
    img: "https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fcdn.wccftech.com%2Fwp-content%2Fuploads%2F2017%2F06%2Fxbox-one-x-2.png&f=1&nofb=1&ipt=c868369c48711dcd031d0359f4551dcd9261da0c7c61107dc5ef38ba450151eb&ipo=images",
    price: 299.99
  },
  {
    name: 'Switch',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.lifewire.com%2Fthmb%2F5OfRviGTIH3fgk4Q0sjjDdQnyJA%3D%2F1920x0%2Ffilters%3Ano_upscale()%3Amax_bytes(150000)%3Astrip_icc()%2Fnintendo-switch-e57b1ba00b1048b592bea7317c741385.jpg&f=1&nofb=1&ipt=b839d7e0961b6f3adf465615467f26f8a6c9b45a5d947dfe3aed86c69cdab6ba&ipo=images",
    price: 199.99
  },
  {
    name: 'Steam Deck',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.cloudflare.steamstatic.com%2Fsteamdeck%2Fimages%2Fsocial_media_image.jpg&f=1&nofb=1&ipt=e0a221fa9c9b5306487767d50c49ee85394c508bf8d021192a413797576afc4c&ipo=images",
    price: 399.99
  },
  {
    name: 'PlayStation 4',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.bhphotovideo.com%2Fimages%2Fimages2500x2500%2Fsony_3003979_days_of_play_limited_1479191.jpg&f=1&nofb=1&ipt=c70e8ea959951ed65585fb48b61a4b9c3e78edea9e0297a1f0226bd4e2fcdc3e&ipo=images",
    price: 299.99
  },
  {
    name: 'Xbox Series X',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi1.wp.com%2Fwildbreaktech.com%2Fwp-content%2Fuploads%2F2020%2F11%2Fxboxgamcon01.png%3Fresize%3D1024%252C1024%26ssl%3D1&f=1&nofb=1&ipt=79a665663fa2c1a9af6b8f288caae5465c882da9bafd264cc7f2633ea53f8df8&ipo=images",
    price: 499.99
  },
  {
    name: 'Nintendo 3DS',
    img: "https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2Ff%2Ff0%2FNintendo-3DS-AquaOpen.jpg&f=1&nofb=1&ipt=dcf126aebe0f57afe579ae184c3f4d6cb1548c6616c4a468b60b0043d5fc4639&ipo=images",
    price: 149.99
  },
  {
    name: 'Switch Lite',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fimages.nintendolife.com%2Fa4bfd70b635bd%2Fswitchlite.large.jpg&f=1&nofb=1&ipt=f754a0e4c775b7e24b65525337958e0ccaf80a96741a374c0cd28434e3423f1b&ipo=images",
    price: 199.99
  },
  {
    name: 'PlayStation 3',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Frukminim1.flixcart.com%2Fimage%2F1664%2F1664%2Fgamingconsole%2Fh%2F3%2F2%2Fplaystation-3-ps3-12-sony-original-imaeqcvbznp2bxyr.jpeg%3Fq%3D90&f=1&nofb=1&ipt=173cdcfb8ed53f8c4fcdca52f3bca09a1b7eda00ebbdab7e0ed77955acaadf10&ipo=images",
    price: 199.99
  },
  {
    name: 'Xbox 360',
    img: "https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2F6%2F67%2FMicrosoft-Xbox-360-E-wController.jpg&f=1&nofb=1&ipt=dddee698908afd38363ae9411e533dca201dcb95d18be104b84580c09763167e&ipo=images",
    price: 99.99
  },
  {
    name: 'Nintendo DS',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2Fthumb%2Fa%2Fa3%2FNintendo-DS-Fat-Blue.png%2F1920px-Nintendo-DS-Fat-Blue.png&f=1&nofb=1&ipt=ef675639724eaca06e043d50701a095ede0425132931b96d1b7ab8cd953a4a17&ipo=images",
    price: 79.99
  },
  {
    name: 'PlayStation Vita',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2Fthumb%2Fb%2Fb4%2FPlayStation-Vita-1101-FL.jpg%2F1200px-PlayStation-Vita-1101-FL.jpg&f=1&nofb=1&ipt=1eec2e932c02d1293fd9a3ac382b2e429ba38c299732e31a7b55a5c799dc6bf4&ipo=images",
    price: 199.99
  },
  {
    name: 'Wii U',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2Fthumb%2F4%2F4a%2FWii_U_Console_and_Gamepad.png%2F1200px-Wii_U_Console_and_Gamepad.png&f=1&nofb=1&ipt=f3ae46c7fcaf7cd69032b99310a225fa3b34091d52f7d8211d63e7b7f98c1d20&ipo=images",
    price: 249.99
  },
  {
    name: 'Xbox One S',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fbrain-images-ssl.cdn.dixons.com%2F1%2F7%2F10183671%2Fu_10183671.jpg&f=1&nofb=1&ipt=2913289b33042cf9b2af6c777a4c56bbfa0c2056e3ea24b83646457971c18d1b&ipo=images",
    price: 299.99
  },
  {
    name: 'Nintendo Wii',
    img: "https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2F1%2F14%2FWii-console.jpg&f=1&nofb=1&ipt=8056de863ef66ad198fab186b7faab6666f1c08f8b0cfea2e8706e879006483e&ipo=images",
    price: 149.99
  },
  {
    name: 'PlayStation 2',
    img: "https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Flowendmac.com%2Fwp-content%2Fuploads%2Fps2-fat.jpg&f=1&nofb=1&ipt=241edeb97c205f4f1a95ec5d40009ee9bd1382e941a84db516929df53f5742fb&ipo=images",
    price: 129.99
  },
  {
    name: 'Xbox One X',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi0.wp.com%2Fwww.theeffect.net%2Fwp-content%2Fuploads%2F2017%2F11%2FXbox_One_X_Screenshot_05.0.jpg&f=1&nofb=1&ipt=b2e9e1be334f2573004193f7f61e158104773863538cb318b34684452247600c&ipo=images",
    price: 499.99
  },
  {
    name: 'Nintendo GameCube',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2F8%2F85%2FGameCube-Silver-Optional-Set.jpg&f=1&nofb=1&ipt=82d0fadc097c372dde7f1c431b33e712076476391cc8c6b1db2d4aca44bc5988&ipo=images",
    price: 99.99
  },
  {
    name: 'Nintendo Switch OLED',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fsharenews.grantdigital.com.au%2Fimages%2FNintendo_Switch_OLED_Model_-_Illustration.jpg&f=1&nofb=1&ipt=e6f24df755cd215a625978cce19e4c7e878e21aafc71eae6866fe9a41f7b4682&ipo=images",
    price: 349.99
  },
  {
    name: 'Nintendo DS Lite',
    img: "https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fupload.wikimedia.org%2Fwikipedia%2Fcommons%2F5%2F56%2FNintendo-DS-Lite-Black-Open.png&f=1&nofb=1&ipt=8a83c19469672db607f3b8f35b7512aaced80183136624bef27b78e3b7a57791&ipo=images",
    price: 69.99
  }
    ],
    cartItems: []
  }),
  methods: {
    addItemToCart(product) {
      this.$emit("addItemToCart", product);
    }
  }
};
</script>

<style scoped>
.consoles {
  display: flex;
  flex-wrap: wrap; 
  text-align: center;
  margin: 10px;
}
.console-image {
  max-width: 250px;
  max-height: 250px;
  min-height: 250px;
  min-width: 250px;
}
</style>
