<script setup>
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Bars3Icon, BookmarkIcon, XMarkIcon } from '@heroicons/vue/24/outline'
import { ArrowPathIcon, CloudArrowUpIcon, LockClosedIcon, AcademicCapIcon, SparklesIcon, ShieldCheckIcon } from '@heroicons/vue/20/solid'
import { defineComponent, h } from 'vue'

const navigation = {
  main: [
    { name: 'Home', href: '#' },
    { name: 'About Us', href: '#AboutUs' },
    { name: 'Corporate Culture', href: '#CorporateCulture' },
    { name: 'Milestone', href: '#Milestone' },
    { name: 'Our Product / Services', href: '#Product' },
    { name: 'Our Partners', href: '#Partners' },
    { name: 'Our Cases', href: '#Cases' },
  ],
  social: [
    {
      name: 'Facebook',
      href: '#',
      icon: defineComponent({
        render: () =>
          h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
            h('path', {
              'fill-rule': 'evenodd',
              d: 'M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z',
              'clip-rule': 'evenodd',
            }),
          ]),
      }),
    },
    {
      name: 'Instagram',
      href: '#',
      icon: defineComponent({
        render: () =>
          h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
            h('path', {
              'fill-rule': 'evenodd',
              d: 'M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z',
              'clip-rule': 'evenodd',
            }),
          ]),
      }),
    },
    {
      name: 'X',
      href: '#',
      icon: defineComponent({
        render: () =>
          h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
            h('path', {
              d: 'M13.6823 10.6218L20.2391 3H18.6854L12.9921 9.61788L8.44486 3H3.2002L10.0765 13.0074L3.2002 21H4.75404L10.7663 14.0113L15.5685 21H20.8131L13.6819 10.6218H13.6823ZM11.5541 13.0956L10.8574 12.0991L5.31391 4.16971H7.70053L12.1742 10.5689L12.8709 11.5655L18.6861 19.8835H16.2995L11.5541 13.096V13.0956Z',
            }),
          ]),
      }),
    },
    {
      name: 'GitHub',
      href: '#',
      icon: defineComponent({
        render: () =>
          h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
            h('path', {
              'fill-rule': 'evenodd',
              d: 'M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z',
              'clip-rule': 'evenodd',
            }),
          ]),
      }),
    },
    {
      name: 'YouTube',
      href: '#',
      icon: defineComponent({
        render: () =>
          h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
            h('path', {
              'fill-rule': 'evenodd',
              d: 'M19.812 5.418c.861.23 1.538.907 1.768 1.768C21.998 8.746 22 12 22 12s0 3.255-.418 4.814a2.504 2.504 0 0 1-1.768 1.768c-1.56.419-7.814.419-7.814.419s-6.255 0-7.814-.419a2.505 2.505 0 0 1-1.768-1.768C2 15.255 2 12 2 12s0-3.255.417-4.814a2.507 2.507 0 0 1 1.768-1.768C5.744 5 11.998 5 11.998 5s6.255 0 7.814.418ZM15.194 12 10 15V9l5.194 3Z',
              'clip-rule': 'evenodd',
            }),
          ]),
      }),
    },
  ]
}

const mobileMenuOpen = ref(false)

const features = [
  {
    name: 'Our Visions',
    description:
      'Bring the most fun, entertained and educational animation to the Chinese Kids to create harmony and joyful atmosphere and feeling to the Kids and parents.',
    href: '#',
    icon: AcademicCapIcon,
  },
  {
    name: 'Our Mission',
    description:
      'To achieve above aim, Joy culture media is committed to establish an extraordinary enterprise specializing in content localization and management of foreign animation brands and development of the Chinese animation as excellent tools for communication with kids and young audiences across China and Asia territory.',
    href: '#',
    icon: SparklesIcon,
  },
  {
    name: 'Our Values',
    description:
      'Hard working, cooperation, innovation and mutual benefit.',
    href: '#',
    icon: ShieldCheckIcon,
  },
]

const milestone = [
  {
    date: '2016.4.1',
    content: 'Beijing Joy Culture Media Company established.'
  },
  {
    date: '2018.6',
    content: 'Launch the CRM system to international brand owner.'
  },
  {
    date: '2019.10',
    content: 'Joy media product brand “Joy Baby” (茁贝) established and launch online.'
  },
  {
    date: '2019.12',
    content: 'Zhejiang Joy culture media company established.'
  },
  {
    date: '2020.03',
    content: '“MOCAS” Season 1 get approved by Zhejiang SARFT as Zhejiang Joy media first Chinese original animated TV series.'
  },
  {
    date: '2020.06',
    content: 'The Fixies Lab Season 1 get approved by Zhejiang SARFT as Zhejiang Joy media first Chinese original children TV drama series.'
  },
  {
    date: '2021. 09',
    content: '"The Fixies Lab" Season 1 premiered on Hebei children TV channels and Tencent Video.'
  },
  {
    date: '2022.05',
    content: '"Play with Mocas" and "Sing with Mocas" were successfully launched in China.'
  },
  {
    date: '2022.10',
    content: 'Joy Media acquired the exclusive rights of Youtube\'s top children\'s live-action show "Like Nastya" in China and successfully launched it exclusively on Tencent Video. The show achieved two billion views in China.'
  },
  {
    date: '2023.05',
    content: 'Joy Media\'s original production, the children\'s program "Cubic Cat(问号猫)," first season was successfully launched in China. This marks the first format of a children\'s program that combines animation with live action in China.'
  },
  {
    date: '2024. 01',
    content: 'Joy Media UK Company Ltd is officially established.'
  },
]

const incentives = [
  {
    name: 'IP Services',
    imageSrc: 'https://www.bjjoymedia.com/img/joymediauk_icon/ip_service.svg',
    description: "It's not actually free we just price it into the products. Someone's paying for it, and it's not us.",
  },
  {
    name: 'Content localization',
    imageSrc: 'https://www.bjjoymedia.com/img/joymediauk_icon/content_localization.svg',
    description: "If it breaks in the first 10 years we'll replace it. After that you're on your own though.",
  },
  {
    name: 'Content distribution',
    imageSrc: 'https://www.bjjoymedia.com/img/joymediauk_icon/content_distribution.svg',
    description:
      "If you don't like it, trade it to one of your friends for something of theirs. Don't send it here though.",
  },
  {
    name: 'Licensing',
    imageSrc: 'https://www.bjjoymedia.com/img/joymediauk_icon/licensing.svg',
    description: "It's not actually free we just price it into the products. Someone's paying for it, and it's not us.",
  },
  {
    name: 'Brand operation',
    imageSrc: 'https://www.bjjoymedia.com/img/joymediauk_icon/brand_operation.svg',
    description: "If it breaks in the first 10 years we'll replace it. After that you're on your own though.",
  },
  {
    name: 'Merchandising sales',
    imageSrc: 'https://www.bjjoymedia.com/img/joymediauk_icon/merchandising_sales.svg',
    description:
      "If you don't like it, trade it to one of your friends for something of theirs. Don't send it here though.",
  },
]

const partner_logo = [
  {
    img: 'https://www.bjjoymedia.com/img/partner-riki.jpg',
    name: 'riki'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-aeroplane.jpg',
    name: 'aeroplane'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-ctc.jpg',
    name: 'ctc'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/zeptolab.png',
    name: 'zeptolab'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-soyuzmultfilm.jpg',
    name: 'soyuzmultfilm'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-pilot.jpg',
    name: 'pilot'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-digitallight.jpg',
    name: 'digitallight'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-noviydisk.jpg',
    name: 'noviydisk'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-redcarpet.jpg',
    name: 'redcarpet'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-uspstudios.jpg',
    name: 'uspstudios'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/bwo.png',
    name: 'bwo'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-planetnemo.jpg',
    name: 'planetnemo'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-projectfirst.jpg',
    name: 'projectfirst'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-brand4rent.jpg',
    name: 'brand4rent'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner-mechtalet.jpg',
    name: 'mechtalet'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/fununion.png',
    name: 'FunUnion'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/hoho.png',
    name: 'Hoho Entertainment'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/dtr.png',
    name: 'DTR'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/dandelooo.png',
    name: 'Dandelooo'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/cbc.png',
    name: 'CBC'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/mediaim.png',
    name: 'MediaIM'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/ABC_Cartoons.png',
    name: 'ABC Cartoons'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/Canny_Factory.png',
    name: 'Canny Factory'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/Magnet_Film.png',
    name: 'Magnet Film'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/Propulsores.png',
    name: 'Propulsores'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/Animaccord.png',
    name: 'Animaccord'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/likenastya.jpg',
    name: 'LikeNastya'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/aardman.png',
    name: 'Aardman'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/themediapioneers.jpg',
    name: 'themediapioneers'
  },
  {
    img: 'https://www.bjjoymedia.com/img/partner/mojicons.jpg',
    name: 'mojicons'
  },

]

const showcase = [
  {
    cover: 'https://pic.imgdb.cn/item/5e774d2e5c56091129d4d34d.jpg',
    alt: 'KID-E-CATS S1',
    title: 'KID-E-CATS S1'
  },
  {
    cover: 'https://pic.imgdb.cn/item/5e774d725c56091129d4fff1.jpg',
    alt: 'KID-E-CATS S2',
    title: 'KID-E-CATS S2'
  },
  {
    cover: 'https://pic.imgdb.cn/item/5e774d895c56091129d50e08.jpg',
    alt: 'The Fixies',
    title: 'The Fixies'
  },
  {
    cover: 'https://pic.imgdb.cn/item/5e774d9c5c56091129d51c2f.jpg',
    alt: 'The Fixies Lab',
    title: 'The Fixies Lab'
  },
  {
    cover: 'https://pic.imgdb.cn/item/5e774da95c56091129d527cc.jpg',
    alt: 'The Fixies Let\'s Play ',
  title:'The Fixies Let\'s Play'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774dc45c56091129d54616.jpg',
	alt: 'Smeshariki S1-S2',
	title: 'Smeshariki S1-S2'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774dd15c56091129d554c6.jpg',
	alt: 'Smeshariki S3',
	title: 'Smeshariki S3'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774ddf5c56091129d5651e.jpg',
	alt: 'PinCode',
	title: 'PinCode'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774df45c56091129d57d98.jpg',
	alt: 'Om Nom Stories',
	title: 'Om Nom Stories'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e035c56091129d58ce6.jpg',
	alt: 'Mojicons',
	title: 'Mojicons'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e115c56091129d59de4.jpg',
	alt: 'BabyRiki S3',
	title: 'BabyRiki S3'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e2a5c56091129d5b5a3.jpg',
	alt: 'Flying Animals',
	title: 'Flying Animals'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e365c56091129d5c3ce.jpg',
	alt: 'Kids And Flying Animals',
	title: 'Kids And Flying Animals'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e465c56091129d5d5ec.jpg',
	alt: 'Homur And Gumur',
	title: 'Homur And Gumur'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e525c56091129d5e4ae.jpg',
	alt: 'Heroes of Envell',
	title: 'Heroes of Envell'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e625c56091129d5f5ad.jpg',
	alt: 'Fantasy Patrol',
	title: 'Fantasy Patrol'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e725c56091129d6085b.jpg',
	alt: 'Leo & Tig',
	title: 'Leo & Tig'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e875c56091129d61e8c.jpg',
	alt: 'Rolando Locomotov',
	title: 'Rolando Locomotov'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774e965c56091129d62e42.jpg',
	alt: 'Opposites Interact',
	title: 'Opposites Interact'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774ea25c56091129d63896.jpg',
	alt: 'Professor Whysenhower',
	title: 'Professor Whysenhower'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774eb95c56091129d64e06.jpg',
	alt: 'Clever Cars S1',
	title: 'Clever Cars S1'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774ec55c56091129d65cd2.jpg',
	title: 'Clever Cars S2'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774ed65c56091129d66f88.jpg',
	alt: 'At the Playground',
	title: 'At the Playground'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774ee55c56091129d67e07.jpg',
	alt: 'Leo the truck',
	title: 'Leo the truck'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774ef45c56091129d68dad.jpg',
	alt: '4 Cars',
	title: '4 Cars'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f045c56091129d6a111.jpg',
	alt: 'Doctor McWheelie S1',
	title: 'Doctor McWheelie S1'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f115c56091129d6ad97.jpg',
	alt: 'Doctor McWheelie S2',
	title: 'Doctor McWheelie S2'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f225c56091129d6bf8f.jpg',
	alt: 'The Bubbles',
	title: 'The Bubbles'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f2e5c56091129d6cc7b.jpg',
	alt: 'Car School S1',
	title: 'Car School S1'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f385c56091129d6d8a2.jpg',
	alt: 'Car School S2',
	title: 'Car School S2'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f4b5c56091129d6ed4c.jpg',
	alt: 'Rosa Dara',
	title: 'Rosa Dara'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f5a5c56091129d6fee6.jpg',
	alt: 'Smarta and Her Magic-Bag S1',
	title: 'Smarta and Her Magic-Bag S1'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f655c56091129d70a62.jpg',
	alt: 'Smarta and Her Magic-Bag S2',
	title: 'Smarta and Her Magic-Bag S2'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f745c56091129d7191f.jpg',
	alt: 'Robodz',
	title: 'Robodz'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f855c56091129d72b0a.jpg',
	alt: 'DollHouse',
	title: 'DollHouse'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774f935c56091129d73808.jpg',
	alt: 'HopHop the Owl',
	title: 'HopHop the Owl'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774fa05c56091129d74458.jpg',
	alt: 'Sing with Leo',
	title: 'Sing with Leo'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774faf5c56091129d75558.jpg',
	alt: 'Funny Clown Videos',
	title: 'Funny Clown Videos'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774fbb5c56091129d76392.jpg',
	alt: 'Blaster Castle',
	title: 'Blaster Castle'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774fc75c56091129d77343.jpg',
	alt: 'Roboborik',
	title: 'Roboborik'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774fd35c56091129d78268.jpg',
	alt: 'Bob The Train',
	title: 'Bob The Train'
},
{
	cover: 'https://pic.imgdb.cn/item/5e774fe05c56091129d78fb1.jpg',
	alt: 'Farmees',
	title: 'Farmees'
},
{
	cover: 'https://pic.imgdb.cn/item/5e7750135c56091129d7c4ce.jpg',
	alt: 'JuniorSquad',
	title: 'JuniorSquad'
},
{
	cover: 'https://pic.imgdb.cn/item/5e7750245c56091129d7d540.jpg',
	alt: 'LittleEddie',
	title: 'LittleEddie'
},
{
	cover: 'https://pic.imgdb.cn/item/5e77502e5c56091129d7dd1b.jpg',
	alt: 'Little Tree House',
	title: 'Little Tree House'
},
{
	cover: 'https://pic.imgdb.cn/item/642faab8a682492fcc1bdd0a.jpg',
	alt: 'Like Nastya',
	title: 'Like Nastya'
},
{
	cover: 'https://pic.imgdb.cn/item/642faab8a682492fcc1bdc8a.jpg',
	alt: 'Blippi',
	title: 'Blippi'
},
{
	cover: 'https://pic.imgdb.cn/item/642faab8a682492fcc1bdcab.jpg',
	alt: 'Blippi Wonders',
	title: 'Blippi Wonders'
},
{
	cover: 'https://pic.imgdb.cn/item/642faab9a682492fcc1bdd80.jpg',
	alt: 'T-Rex Ranch',
	title: 'T-Rex Ranch'
},
{
	cover: 'https://pic.imgdb.cn/item/642faab8a682492fcc1bdc57.jpg',
	alt: 'Beardy Bodo',
	title: 'Beardy Bodo'
},
{
	cover: 'https://pic.imgdb.cn/item/642faab8a682492fcc1bdce9.jpg',
	alt: 'Dino City',
	title: 'Dino City'
},
{
	cover: 'https://pic.imgdb.cn/item/642faab9a682492fcc1bdd5e.jpg',
	alt: 'The Very Small Creatures',
	title: 'The Very Small Creatures'
},
{
	cover: 'https://pic.imgdb.cn/item/642faab9a682492fcc1bdd47.jpg',
	alt: 'The Epic Adventures of Morph',
	title: 'The Epic Adventures of Morph'
},
{
	cover: 'https://pic.imgdb.cn/item/642faab9a682492fcc1bdd1c.jpg',
	alt: 'SEALOOK',
	title: 'SEALOOK'
},

]

function clickNav() {
  alert('Currently under construction.')
}
</script>

<template>
  <div class="bg-white">
    <header class="absolute inset-x-0 top-0 z-50">
      <nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Joymedia Uk</span>
            <img class="h-8 w-auto" src="https://www.bjjoymedia.com/img/logo.png" alt="Joymedia Uk" />
          </a>
        </div>
        <div class="flex lg:hidden">
          <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = true">
            <span class="sr-only">Open main menu</span>
            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a v-for="item in navigation.main" :key="item.name" :href="item.href" class="text-sm font-semibold leading-6 text-gray-900">{{ item.name }}</a>
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end">
          <!-- <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Chinese<span aria-hidden="true">&rarr;</span></a> -->
        </div>
      </nav>
      <Dialog as="div" class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
        <div class="fixed inset-0 z-50" />
        <DialogPanel class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
          <div class="flex items-center justify-between">
            <a href="#" class="-m-1.5 p-1.5">
              <span class="sr-only">Joymedia Uk</span>
              <img class="h-8 w-auto" src="https://www.bjjoymedia.com/img/logo.png" alt="Joymedia UK" />
            </a>
            <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
              <span class="sr-only">Close menu</span>
              <XMarkIcon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <a v-for="item in navigation.main" :key="item.name" :href="item.href" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">{{ item.name }}</a>
              </div>
              <!-- <div class="py-6">
                <a href="#" class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Log in</a>
              </div> -->
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>

    <div class="relative isolate px-6 pt-14 lg:px-8">
      <div class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80" aria-hidden="true">
        <div class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
      </div>
      <div class="mx-auto max-w-6xl py-32">
        <div id="AboutUs">
          <h1 class="text-3xl font-bold tracking-tight text-gray-900">About Us</h1>
          <p class="mt-6 leading-8 text-gray-600 text-left">Joy Culture Media (JCM) is an internationally leading children animation and home entertainment IP production, operation and marketing company headquartered in Beijing, China.</p>
          <p class="mt-6 leading-8 text-gray-600 text-left">Beijing Joy Culture Media Co., Ltd is established in 2016, as a global Intellectual Property licensing company in Beijing that acquires and commercializes children animation IP over the world, discovering new and progressive content that improve the overall quality of children life in China. Up to 2024, the company has cooperate with over 40 animation companies all over the world,exclusively sub-license over 120 IPs in mainland China territory, total length of the animation program is over 1000hours,total views on new media platforms is over 20billion, there are over 100 animated TV series which is very well known among Chinese children has been exclusively distribute by Joy media such as The Fixies, Kid E Cats, Little Tiaras, Like Nastya, Sealook, Be-Be-Bear, Fantasy Patrol, Masha’s Spooky Stories, Masha’s Songs, 4 Cars and Cloud Babies.</p>
          <p class="mt-6 leading-8 text-gray-600 text-left">Zhejiang Joy Culture Media Co.Ltd is a brand new company registered in 2019 delicate in Chinese original animated TV series production, international co-production and Children TV drama series production, operation and marketing. The first Chinese original animated TV series MOCAS target with 3-5 years old preschooler has launched in market and achieved great positive feedback from the market, the first Children TV drama series The Fixies lab is Joy media first successful case to adopt a foreign children animation IP into a local Chinese children TV drama series, the Fixies Lab S1 completed and launched in Sep 2021 and launched on Tecent video and five children TV channels in China.</p>
        </div>
      </div>
      <div class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
        <div class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
      </div>
    </div>
    <!-- 企业文化 -->
    <div id="CorporateCulture" class="bg-white">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl lg:text-center">
          <!-- <h2 class="text-base font-semibold leading-7 text-indigo-600">Deploy faster</h2> -->
          <h3 class="mt-2 text-3xl font-bold tracking-tight text-gray-900">Corporate Culture</h3>
          <!-- <p class="mt-6 text-lg leading-8 text-gray-600">Quis tellus eget adipiscing convallis sit sit eget aliquet quis. Suspendisse eget egestas a elementum pulvinar et feugiat blandit at. In mi viverra elit nunc.</p> -->
        </div>
        <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-none">
          <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-16 lg:max-w-none lg:grid-cols-3">
            <div v-for="feature in features" :key="feature.name" class="flex flex-col">
              <dt class="flex items-center gap-x-3 text-base font-semibold leading-7 text-gray-900">
                <component :is="feature.icon" class="h-5 w-5 flex-none text-indigo-600" aria-hidden="true" />
                {{ feature.name }}
              </dt>
              <dd class="mt-4 flex flex-auto flex-col text-base leading-7 text-gray-600 text-left">
                <p class="flex-auto">{{ feature.description }}</p>
                <!-- <p class="mt-6">
                  <a :href="feature.href" class="text-sm font-semibold leading-6 text-indigo-600">Learn more <span aria-hidden="true">→</span></a>
                </p> -->
              </dd>
            </div>
          </dl>
        </div>
      </div>
    </div>
    <!-- 时间线 -->
    <div id="Milestone" class="mx-auto max-w-2xl lg:text-center py-32">
      <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900">Milestone</p>
    </div>
    <div class="flex flex-col md:grid grid-cols-9 mx-auto p-2 text-gray-600">
      <div v-for="(item, index) in milestone" :key="index" :class="{ 'flex text-left md:contents': index % 2 === 1, 'flex flex-row-reverse text-left md:text-right lg:text-right md:contents': index % 2 === 0 }">
        <template v-if="index % 2 === 0">
          <!-- left -->
          <div class="flex flex-row-reverse text-left md:text-right lg:text-right md:contents">
            <div class="col-start-1 col-end-5 p-4 my-4 ml-auto">
              <h3 class="font-semibold text-lg mb-1">{{ item.date }}</h3>
              <p class="leading-7">{{ item.content }}</p>
            </div>
            <div class="col-start-5 col-end-6 md:mx-auto relative mr-10">
              <div class="h-full w-6 flex items-center justify-center">
                <div class="h-full w-1 bg-blue-800 pointer-events-none"></div>
              </div>
              <div class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-blue-500 shadow"></div>
            </div>
          </div>
        </template>
        <template v-if="index % 2 === 1">
          <!-- right -->
          <div class="flex text-left md:contents">
            <div class="col-start-5 col-end-6 mr-10 md:mx-auto relative">
              <div class="h-full w-6 flex items-center justify-center">
                <div class="h-full w-1 bg-blue-800 pointer-events-none"></div>
              </div>
              <div class="w-6 h-6 absolute top-1/2 -mt-3 rounded-full bg-blue-500 shadow"></div>
            </div>
            <div class="col-start-6 col-end-10 p-4 my-4 mr-auto">
              <h3 class="font-semibold text-lg mb-1">{{ item.date }}</h3>
              <p class="leading-7">{{ item.content }}</p>
            </div>
          </div>
        </template>
      </div>
    </div>
    <!-- service -->
    <div id="Product" class="mx-auto max-w-7xl px-4 py-24 sm:px-6 lg:px-8">
      <div class="rounded-2xl bg-gray-50 px-6 py-16 sm:p-16">
        <div class="mx-auto max-w-xl lg:max-w-none">
          <div class="text-center py-10">
            <h2 class="text-3xl font-bold tracking-tight text-gray-900 m-">Our Product / Services</h2>
          </div>
          <div class="mx-auto mt-12 grid max-w-sm grid-cols-1 gap-x-8 gap-y-10 sm:max-w-none lg:grid-cols-6">
            <div v-for="incentive in incentives" :key="incentive.name" class="text-center sm:flex sm:text-left lg:block lg:text-center">
              <div class="sm:flex-shrink-0">
                <div class="flow-root">
                  <img class="mx-auto h-16 w-16" :src="incentive.imageSrc" alt="" />
                </div>
              </div>
              <div class="mt-3 sm:ml-6 sm:mt-0 lg:ml-0 lg:mt-6">
                <h3 class="text-sm font-medium text-gray-900">{{ incentive.name }}</h3>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- TV Distribution License & Awards -->
    <div id="Partners" class="relative isolate">
      <div class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80" aria-hidden="true">
        <div class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
      </div>
      <div class="py-24 sm:py-12">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
          <div class="mx-auto max-w-2xl text-center">
            <h2 class="text-3xl font-bold tracking-tight text-gray-900">TV Distribution License & Awards</h2>
            <p class="mt-6 text-lg leading-8 text-gray-600">Taking brand Smeshariki as an example.</p>
          </div>
          <div class="mt-16 flow-root sm:mt-24">
            <img src="https://www.bjjoymedia.com/img/en-licenese-awards.jpg" alt="App screenshot" width="877" height="294" class="rounded-md ring-1 ring-gray-900/10 m-auto" />
          </div>
        </div>
        <div class="mx-auto max-w-7xl pt-40">
          <div class="mx-auto max-w-2xl text-center">
            <h2 class="text-3xl font-bold tracking-tight text-gray-900">Our Partners</h2>
          </div>
          <div class="mt-16 flow-root sm:mt-24">
            <img src="https://www.bjjoymedia.com/img/en-our-partners.png" alt="App screenshot" width="446" height="451" class="rounded-md m-auto" />
          </div>
        </div>
      </div>
      <!-- logo -->
      <div class="py-24">
        <div class="mx-auto max-w-7xl">
          <div class="mx-auto max-w-2xl text-center">
            <h2 class="text-3xl font-bold tracking-tight text-gray-900">Media platforms</h2>
          </div>
        </div>
      </div>
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="-mx-6 grid grid-cols-2 gap-0.5 overflow-hidden sm:mx-0 sm:rounded-2xl md:grid-cols-6">
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-vqq.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-youku.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-iqiyi.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-xiaomi.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-cctv14.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-ixigua.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-ximalaya.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-mangguo.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-newtv.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-huashu.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-huashi.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-guokaitongmei.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-beva.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-tvjoy.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-puxin.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-babybus.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-douyin.jpg" alt="" width="198" height="100" />
          </div>
          <div class="bg-gray-400/5 p-4">
            <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-xiaohongshu.jpg" alt="" width="198" height="100" />
          </div>
        </div>
      </div>


      <div class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
        <div class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
      </div>
    </div>
    <!-- 合作版权方logo -->
    <div class="py-24">
      <div class="mx-auto max-w-7xl">
        <div class="mx-auto max-w-2xl text-center">
          <h2 class="text-3xl font-bold tracking-tight text-gray-900">International Partners</h2>
        </div>
      </div>
    </div>
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="-mx-6 grid grid-cols-2 gap-0.5 overflow-hidden sm:mx-0 sm:rounded-2xl md:grid-cols-6"> 
        <div v-for="item in partner_logo" :key="item.name" class="bg-gray-400/5 p-4">
          <img class="w-full object-contain" :src="item.img" :alt="item.name" width="198" height="100" />
        </div>
      </div>
    </div>
    <!-- 合作展会 -->
    <div class="py-24">
      <div class="mx-auto max-w-7xl">
        <div class="mx-auto max-w-2xl text-center">
          <h2 class="text-3xl font-bold tracking-tight text-gray-900">Expo Partners</h2>
        </div>
      </div>
    </div>
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="-mx-6 grid grid-cols-2 gap-0.5 overflow-hidden sm:mx-0 sm:rounded-2xl md:grid-cols-6"> 
        <div class="bg-gray-400/5 p-4">
          <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-cicaf.jpg" width="198" height="100" />
        </div>
        <div class="bg-gray-400/5 p-4">
          <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-iabc.jpg" width="198" height="100" />
        </div>
        <div class="bg-gray-400/5 p-4">
          <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-lec.jpg" width="198" height="100" />
        </div>
        <div class="bg-gray-400/5 p-4">
          <img class="w-full object-contain" src="https://www.bjjoymedia.com/img/partner-annecy.jpg" width="198" height="100" />
        </div>
      </div>
    </div>
    <!-- 联系方式 -->
    <div class="mx-auto max-w-7xl pt-20">
      <div class="mx-auto max-w-2xl text-center">
        <h3 class="text-3xl font-bold tracking-tight text-gray-900">Contact Us</h3>
      </div>
      <div class="mt-16 flow-root sm:mt-24">
        <img src="https://www.bjjoymedia.com/img/info-email-black.png" alt="App screenshot" width="227" height="23" class="rounded-md m-auto" />
      </div>
    </div>
    <!-- show case -->
    <div id="Cases" class="mx-auto max-w-7xl pt-20">
      <div class="mx-auto max-w-2xl text-center">
        <h3 class="text-3xl font-bold tracking-tight text-gray-900">Our Cases</h3>
      </div>
      <div class="mt-16 flow-root">
      </div>
    </div>
    <ul role="list" class="grid grid-cols-9 gap-x-4 gap-y-4">
      <li v-for="item in showcase" :key="item.cover" class="relative">
        <div class="group block overflow-hidden rounded-md bg-gray-100">
          <img :src="item.cover" :alt="item.alt" :title="item.title" class="w-full pointer-events-none object-cover" />
        </div>
      </li>
    </ul>
    <!-- 页脚 -->
    <footer class="bg-white">
      <div class="mx-auto max-w-7xl overflow-hidden px-6 py-20 sm:py-24 lg:px-8">
        <nav class="-mb-6 columns-2 sm:flex sm:justify-center sm:space-x-12" aria-label="Footer">
          <div v-for="item in navigation.main" :key="item.name" class="pb-6">
            <a :href="item.href" class="text-sm leading-6 text-gray-600 hover:text-gray-900">{{ item.name }}</a>
          </div>
        </nav>
        <!-- <div class="mt-10 flex justify-center space-x-10">
          <a v-for="item in navigation.social" :key="item.name" @click="clickNav" class="text-gray-400 hover:text-gray-500">
            <span class="sr-only">{{ item.name }}</span>
            <component :is="item.icon" class="h-6 w-6" aria-hidden="true" />
          </a>
        </div> -->
        <p class="mt-10 text-center text-xs leading-5 text-gray-500">&copy; 2024 Joy Media UK Company Ltd All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>


<style scoped>
</style>
