<template>
    <Page backgroundColor="#3c495e">
        <ActionBar backgroundColor="#3c495e" flat="true" title="My first app"/>
        <StackLayout class="screen" backgroundColor="3c495e">
            <StackLayout class="screen__content content" height="90%" text="first-content" backgroundColor="3c495e">
                <Label text="content" color="white"/>
            </StackLayout>
            <StackLayout  class="screen__menu-buttons menu-buttons" backgroundColor="3c495e" height="10%" orientation="horizontal">
                <StackLayout class="menu-buttons__button" width="20%" text="1 button" backgroundColor="white">
                    <AbsoluteLayout @tap="setCurrentPage('home')" class="menu-buttons__item">
                        <Image class="menu-buttons__icon" :src="currentPage === 'home' ? iconsSrc.homeActive : iconsSrc.home"
                            top="10%" left="10%"
                        />
                        <Label :class="currentPage === 'home' ? 'menu-buttons__text--active' : 'menu-buttons__text'"
                            text="Дом" backgroundColor="white" top="50%" left="16%"
                        />
                    </AbsoluteLayout>
                </StackLayout>
                <StackLayout class="menu-buttons__button" width="20%" backgroundColor="white">
                    <AbsoluteLayout @tap="setCurrentPage('bath')" class="menu-buttons__item">
                        <Image class="menu-buttons__icon" :src="currentPage === 'bath' ? iconsSrc.bathActive : iconsSrc.bath"
                            top="10%" left="12%"
                        />
                        <Label :class="currentPage === 'bath' ? 'menu-buttons__text--active' : 'menu-buttons__text'"
                            text="Ванна" backgroundColor="white" top="50%" left="15%"
                        />
                    </AbsoluteLayout>
                </StackLayout>
                <StackLayout class="menu-buttons__button" width="20%" backgroundColor="white">
                    <AbsoluteLayout @tap="setCurrentPage('tent')" class="menu-buttons__item">
                        <Image class="menu-buttons__icon" :src="currentPage === 'tent' ? iconsSrc.tentActive : iconsSrc.tent"
                        top="12%" left="18%"
                        />
                        <Label :class="currentPage === 'tent' ? 'menu-buttons__text--active' : 'menu-buttons__text'"
                            text="Палатка" backgroundColor="white" top="50%" left="15%"
                        />
                    </AbsoluteLayout>
                </StackLayout>
                <StackLayout class="menu-buttons__button" width="20%" backgroundColor="white">
                    <AbsoluteLayout @tap="setCurrentPage('bycicle')" class="menu-buttons__item">
                        <Image class="menu-buttons__icon" :src="currentPage === 'bycicle' ? iconsSrc.bycicleActive : iconsSrc.bycicle"
                        top="15%" left="24%"
                        />
                        <Label :class="currentPage === 'bycicle' ? 'menu-buttons__text--active' : 'menu-buttons__text'"
                            text="Велосипед" backgroundColor="white" top="50%" left="15%"
                        />
                    </AbsoluteLayout>
                </StackLayout>
                <StackLayout class="menu-buttons__button" width="20%" backgroundColor="white">
                    <AbsoluteLayout @tap="setCurrentPage('more')" class="menu-buttons__item">
                        <Image class="menu-buttons__icon" :src="currentPage === 'more' ? iconsSrc.moreActive : iconsSrc.more"
                        top="10%" left="10%"
                        />
                        <Label :class="currentPage === 'more' ? 'menu-buttons__text--active' : 'menu-buttons__text'"
                            text="Ещё" backgroundColor="white" top="50%" left="16%" 
                        />
                    </AbsoluteLayout>
                </StackLayout>
            </StackLayout>
        </StackLayout>
    </Page>
</template>

<script>
  export default {
    data() {
      return {
        msg: 'Hello World!',
        currentPage: 'home',
        iconsSrc: {
            home: `~/assets/images/menu-buttons/home.png`,
            homeActive: `~/assets/images/menu-buttons/home_active.png`,
            bath: `~/assets/images/menu-buttons/bath.png`,
            bathActive: `~/assets/images/menu-buttons/bath_active.png`,
            tent: `~/assets/images/menu-buttons/tent.png`,
            tentActive: `~/assets/images/menu-buttons/tent_active.png`,
            bycicle: `~/assets/images/menu-buttons/bycicle.png`,
            bycicleActive: `~/assets/images/menu-buttons/bycicle_active.png`,
            more: `~/assets/images/menu-buttons/more.png`,
            moreActive: `~/assets/images/menu-buttons/more_active.png`,
        },
      }
    },

    methods: {
        setCurrentPage: function (page) {
            return this.currentPage = page
        }
    }
  }
</script>

<style lang="scss" scoped>
.menu-buttons{
    background-color: whitesmoke;

    &__text{
        color: gray;

        &--active{
            color: black;
        }
    }

    &__icon{
    }
}
</style>
