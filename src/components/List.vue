<template>
  <div class="listChapter">
    <div class="row" v-for="item in items" :key="item.id">
      <a :href="item.link" class="link" style="text-decoration: none">
        <div class="listChapter__item item-listChapter rounded">
          <div class="item-listChapter__img">
            <img :src="item.imgUrl" :alt="item.altImg" class="rounded" />
          </div>
          <div class="item-listChapter__content">
            <div class="item-listChapter__title">{{ item.title }}</div>
            <div class="item-listChapter__subtitle">{{ item.text }}</div>
            <div class="item-listChapter__time">{{ item.time }}</div>
          </div>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          id: 1,
          imgUrl: require("../assets/images/slider/1.jpg"),
          altImg: "some",
          title: "Title",
          text: "Lorem lorem lorem lorem Lorem lorem lorem lorem",
          link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh",
          time: "45",
        },
        {
          id: 2,
          imgUrl: require("../assets/images/slider/2.png"),
          altImg: "some",
          title: "Title",
          text: "Lorem lorem lorem lorem Lorem lorem lorem lorem",
          link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh",
          time: "435",
        },
        {
          id: 3,
          imgUrl: require("../assets/images/slider/3.png"),
          altImg: "some",
          title: "Title",
          text: "Lorem lorem lorem lorem Lorem lorem lorem lorem",
          link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh",
          time: "425",
        },
        {
          id: 4,
          imgUrl: require("../assets/images/slider/1.jpg"),
          altImg: "some",
          title: "Title",
          text: "Lorem lorem lorem lorem Lorem lorem lorem lorem",
          link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh",
          time: "435",
        },
        {
          id: 5,
          imgUrl: require("../assets/images/slider/1.jpg"),
          altImg: "some",
          title: "Title",
          text: "Lorem lorem lorem lorem Lorem lorem lorem lorem",
          link: "https://yummyanime.club/catalog/item/tvoya-aprel-skaya-lozh",
          time: "445",
        },
      ],
    };
  },
};
</script>


<style lang="scss" scoped>
.listChapter {
  margin-top: 5rem;
  &__item {
  }
}
.row {
  text-decoration: none;
}
.item-listChapter {
  display: flex;
  margin: 0 0 10px 0;
  background: #171717;
  padding: 5px;
  box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);
  @media (max-width: 340px) {
    flex-direction: column;
    text-align: center;
  }
  &__img {
    padding: 0 15px 0 0;
    @media (max-width: 340px) {
      padding: 0px;
    }
  }
  &__img img {
    width: 140px;
    height: auto;
  }

  &__content {
    display: flex;
    flex-direction: column;
    @media (max-width: 340px) {
      padding: 10px 0 0 0;
    }
  }

  &__title {
    @include adaptive_font(17, 14);
    text-decoration: none;
    color: #ffffff;
  }

  &__subtitle {
    @include adaptive_font(15, 13);
    text-decoration: none;
    color: #ffffff;
    flex: 1 1 auto;
    padding: 5px 0 0 0;
    @media (max-width: 340px) {
      padding: 0px;
    }
  }

  &__time {
    @include adaptive_font(12, 10);
    color: darkgray;
    text-decoration: none;
  }
  .item-listChapter:last-child {
    margin: 0px;
  }
  .link {
    text-decoration: none;
  }
}
</style>

