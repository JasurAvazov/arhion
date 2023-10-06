<script setup>
import TheMain from '../components/TheMain.vue'
import OurServiсes from '../components/OurServiсes.vue';
import OurProjects from '../components/OurProjects.vue';
import TheArticle from '../components/TheArticle.vue';
import TheBanner from '../components/TheBanner.vue'
import WithUs from '../components/WithUs.vue';
import ReviewUs from '../components/ReviewUs.vue';
import OurRating from '../components/OurRating.vue';
import OurStatistics from '../components/OurStatistics.vue';
import TheAnswers from '../components/TheAnswers.vue';
import TheAdvice from '../components/TheAdvice.vue';
import TheFooter from '../components/TheFooter.vue';

const article = {
  zero: {
    title: 'Нужен проект',
    subtitle: 'Индувидуальное проектирование',
    text: 'Продолжить вдохновляться - перейдите на страницу индивидуального проектирования, где вы сможете сделать каждую деталь вашего будущего дома выразительной, олицетворяющей вас. Откройте двери в мир творчества и возможностей.',
    bgLink: '../src/assets/images/jpg/articleZero.jpg',
    btnText: 'Воплотите свои мечты'
  },
  first: {
    title: 'Нужен дом',
    subtitle: 'Строительство дома',
    text: 'Добро пожаловать в мир, где ваши мечты о собственном доме становятся реальностью. Мы - команда профессионалов, готовых помочь вам построить дом вашей мечты, который будет не просто строением, а истинным проявлением вашей личности и комфорта.',
    bgLink: '../src/assets/images/jpg/articleFirst.jpg',
    btnText: 'Рассчитать смету'
  },
  second: {
    title: 'Красота и уют',
    subtitle: 'Дизайн интерьера',
    text: 'Добро пожаловать в мир дизайна интерьера, где каждый уголок вашего дома становится произведением искусства. Мы - команда опытных дизайнеров, готовых сделать ваш дом уникальным и уютным.',
    bgLink: '../src/assets/images/jpg/articleSecond.jpg',
    btnText: 'Узнать подробнее'
  },
  third: {
    title: 'Качество',
    subtitle: 'Внутренняя отделка',
    text: 'Добро пожаловать в мир, где каждая деталь имеет значение. Мы специализируемся на внутренней отделке домов, превращая пустые стены в уютные и стильные интерьеры, которые отражают вашу личность и комфорт.',
    bgLink: '../src/assets/images/jpg/articleThird.jpg',
    btnText: 'Узнать подробнее'
  },
  fourth: {
    title: 'Гармония',
    subtitle: 'Ландшафтный дизайн',
    text: 'Добро пожаловать в мир ландшафтного дизайна, где мы превратим ваш участок в живописный рай. Создайте гармонию природы и архитектуры с нашими экспертами по ландшафтному дизайну.',
    bgLink: '../src/assets/images/jpg/articleFourth.jpg',
    btnText: 'Узнать подробнее'
  },
  fifth: {
    title: 'Надежность',
    subtitle: 'Стройматериалы',
    text: 'Новые высококачественные строительные материалы – ваш путь к надежным и красивым строениям! С нами ваш проект станет реальностью. Постройте с уверенностью!',
    bgLink: '../src/assets/images/jpg/articleFifth.jpg',
    btnText: 'Перейти в каталог'
  },
  sixth: {
    title: 'Элегантность',
    subtitle: 'Мебель',
    text: 'Обновите свой дом с нашей эксклюзивной мебелью высшего качества! У нас вы найдете все, чтобы сделать ваш интерьер уютным и элегантным.',
    bgLink: '../src/assets/images/jpg/articleSixth.jpg',
    btnText: 'Перейти в каталог'
  },
  seventh: {
    title: 'Великолепие',
    subtitle: 'Декор для дома',
    text: 'Вдохновляйтесь красотой каждого уголка своего дома с нашим эксклюзивным декором! Мы предлагаем широкий выбор элементов интерьера, которые придадут вашему дому неповторимый шарм и уют.',
    bgLink: '../src/assets/images/jpg/articleSeventh.jpg',
    btnText: 'Перейти в каталог'
  },
  eighth: {
    title: 'Умиротворение',
    subtitle: 'Декор для сада',
    text: 'Преобразите свой сад в волшебное место с нашим эксклюзивным садовым декором! Мы предлагаем широкий выбор украшений, которые придадут вашему саду уникальный вид и создадут уютную атмосферу.',
    bgLink: '../src/assets/images/jpg/articleEighth.jpg',
    btnText: 'Перейти в каталог'
  },
};

const banner = {
  first: {
    title: 'Сочетание креативности и функциональности в каждом дизайне',
    bgLink: '../src/assets/images/png/bannerFirst.png'
  },
  second: {
    title: 'Создаем пространства, в которых вы ощущаете себя дома',
    bgLink: '../src/assets/images/png/bannerSecond.png'
  },
  third: {
    title: 'Дизайн, который меняет мир вокруг вас',
    bgLink: '../src/assets/images/png/bannerThird.png'
  }
}
</script>

<template>
  <TheMain></TheMain>
  <OurServiсes></OurServiсes>
  <TheArticle :content="article.zero"></TheArticle>
  <OurProjects></OurProjects>
  <TheArticle :content="article.first"></TheArticle>
  <WithUs></WithUs>
  <TheArticle :content="article.second"></TheArticle>
  <TheBanner :content="banner.first"></TheBanner>
  <TheArticle :content="article.third"></TheArticle>
  <ReviewUs></ReviewUs>
  <TheArticle :content="article.fourth"></TheArticle>
  <OurRating></OurRating>
  <TheArticle :content="article.fifth"></TheArticle>
  <TheBanner :content="banner.second"></TheBanner>
  <TheArticle :content="article.sixth"></TheArticle>
  <OurStatistics></OurStatistics>
  <TheArticle :content="article.seventh"></TheArticle>
  <TheBanner :content="banner.third"></TheBanner>
  <TheArticle :content="article.eighth"></TheArticle>
  <TheAnswers></TheAnswers>
  <TheAdvice></TheAdvice>
  <TheFooter></TheFooter>
</template>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';
</style>