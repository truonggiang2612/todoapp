<template>
  <div class="slideout" :class="{ active: isOpen}">  <!--class active sẽ dc áp dụng tùy vào tính đúng sai của thuộc tính isOpen  -->
        <div class="opener" @click="toggle">{{openText}}</div>
        <ul class="slideout-menu">
            <li>
                <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/19332/zap-emoji.svg" alt="logo">
            </li>
            <li class="menu" v-for="(item, index) in menu" :key="index">{{item}}</li>
            <li class="small-menu" v-for="(item, index) in smallMenu" :key="index">{{item}}</li>
        </ul>
  </div>
</template>

<script>
export default {
    name: 'ComponentSlideMenu',
    data() {
        return {
            openText: 'Open',
            isOpen: false,
            menu: ['Home', 'Product', 'Contact'],
            smallMenu: ['Tips', 'Description', 'Price']
        }
    },

    methods: {
        openMenu() {
            this.openText = 'Close'
            this.isOpen = true
        },

        closeMenu() {
            this.openText = 'Open'
            this.isOpen = false
        },

        toggle() {
            if (this.isOpen) {
                this.closeMenu()
            } else {
                this.openMenu()
            }
        }
    }
}
</script>

<style>
.slideout {
    position: relative;
    width: 250px;
    height: auto;
    background-color: #34495e;
    transform: translateX(-100%);
    border-radius: 10px;
    transition: 0.7s;
}

.opener {
    position: absolute;
    color: white;
    opacity: 0.7;
    text-transform: uppercase;
    font-weight: 600;
    top: 20px;
    left: 100%;
    font-size: 25px;
    transition: 0.4s;
    margin-left: 20px;
    cursor: pointer;
}

.opener:hover {
    opacity: 1;
}

.active {
    transform: translateX(0);
}

.slideout-menu {
    color: #ccc;
    list-style: none;
    padding: 10px 0;
}

.slideout-menu li img {
    width: 150px;
    height: auto;
    object-fit: cover;
}

.menu {
    font-size: 45px;
    margin-bottom: 10px;
    transition: 0.4s;
}
.menu:hover {
    cursor: pointer;
    color: #FFA500;
}

.small-menu {
    margin-bottom: 10px;
    font-size: 25px;
    transition: 0.4s;
}
.small-menu:hover {
    cursor: pointer;
    color: #FFA500;
}
</style>