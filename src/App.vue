<template>
  <nav>
    
  </nav>
  <header class="header">
        <div class="header__links header__links1">
            <router-link class="header__link" to="/">Домашняя</router-link> 
            <a href="/#about" class="header__link">О компании</a>
            <a href="/#contacts" class="header__link">Контакты</a>
        </div>
        <img src="./assets/img/header__logo.png" alt="EraCars" class="header__logo">
        <div class="header__links header__links2">
            <a href="#" class="header__link">Каталог</a>
            <router-link to="/reki" class="header__link">Реквизиты</router-link>
            <a href="tel:79215850350" class="header__link">тел: +7 (921) 585-03-50</a>
        </div>
          <div id="sidemenu">
        <button class="sidemenu__btn" v-on:click="navOpen = !navOpen" v-bind:class="{ active: navOpen }">
    				
    				<span class="mid"></span>
    				<span class="bottom"></span>
    			</button>
        <transition name="translateX">
          <nav v-show="navOpen">
            <div class="sidemenu__wrapper">
              <ul class="sidemenu__list">
                <li class="sidemenu__item"><router-link to="/">Домашняя</router-link></li>
                <li class="sidemenu__item"><a href="/#about">О компании</a></li>
                <li class="sidemenu__item"><a href="/#contacts">Контакты</a></li>
                <li class="sidemenu__item"><a href="">Каталог</a></li>
                <li class="sidemenu__item"><router-link to="/reki">Реквизиты</router-link></li>
              </ul>
            </div>
          </nav>
        </transition>
        </div>
    
    </header>
  <router-view/>
    <footer class="footer">
        <h1 class="text">© made by Hedgehog design</h1>
    </footer>
</template>
<script>

export default {
    name: 'app',
     data() {
        return {
            navOpen: true,
        }
     },
 
}
</script>
<style lang="scss">
#sidemenu {
	nav {
		width: 200px;
		// height: calc(100% - #{$headerHeight} - #{$footerHeight});
		background: grey;
		position: fixed;
		top: 0;
		left: 0;
		z-index: 99;
		// box-shadow: 2px 0 3px$grey-6;
		// overflow-y: scroll;
	}

	.sidemenu {
		&__btn {
			display: block;
			width: 50px;
			height: 50px;
			background: grey;
			border: none;
			position: relative;
			z-index: 100;
			appearance: none;
			cursor: pointer;
			outline: none;

			span {
				display: block;
				width: 20px;
				height: 2px;
				margin: auto;
				background: white;
				position: absolute;
				top: 0;
				bottom: 0;
				left: 0;
				right: 0;
				transition: all .4s ease;

				&.top {
					transform: translateY(-8px);
				}

				&.bottom {
					transform: translateY(8px);
				}
			}
			&.active{
				.top {
					transform: rotate(-45deg);
                    
				}
				.mid{
					transform: translateX(-20px) rotate(360deg);
					opacity: 0;
				}
				.bottom {
					transform: rotate(45deg);
				}
			}

		}

		&__wrapper {
      padding-top: 50px;
    }

		&__list {
			padding-top: 50px;
      list-style:none;
      padding: 0;
      margin: 0;
		}

		&__item {
			a {
        text-decoration: none;
				line-height: 1.6em;
				font-size: 1.6em;
				padding: .5em;
				display: block;
				color: white;
				transition: .4s ease;

				&:hover {
					background: lightgrey;
					color: dimgrey;
				}
			}
		}
	}
}

.translateX-enter{
	transform:translateX(-200px);
	opacity: 0;
}

.translateX-enter-active,.translateX-leave-active{
	transform-origin: top left 0;
	transition:.2s ease;
}

.translateX-leave-to{
	transform: translateX(-200px);
	opacity: 0;
}

 .logo {
   align-self: center;
   color: #fff;
   font-weight: bold;
   font-family: 'Lato'
 }

.header{
    height: 100px ;
    align-content: center;
    align-items: center;
    justify-content: center;
    width: 100%;
    gap: 200px;
    display: flex;
    position: sticky;
    position: -webkit-sticky;
    z-index: 999;
    top: 0px;
    background-color: black;
    &__links{
        display: flex;
        gap: 20px;
    }
    &__links1{
        justify-content: start;
        

    }
    &__links2{
        justify-content: end;
    }
    &__link{
        font-family: arial;
        color: white;
    }
    &__logo{
        width: 220px;
        height: 26px;
        display: flex;
        justify-content: center;
        background-size: cover;
    }
}
.rates{
    display: flex;
  justify-content: center;
  background-color: whitesmoke;
}
.footer{
    width: 100%;
    height: 150px;
    display: flex;
    background-color: #000;
    justify-content: center;
}
.text{
    display: flex;
    
    color: #fff;
    font-family: Arial;
    font-size: 20px;
    justify-content: center;
    align-content: center;
    align-items: center;
}
 .main-nav {
   display: flex;
   justify-content: space-between;
   padding: 0.5rem 0.8rem;
 }

 ul.sidebar-panel-nav {
   list-style-type: none;
 }

 ul.sidebar-panel-nav > li > a {
   color: #fff;
   text-decoration: none;
   font-size: 1.5rem;
   display: block;
   padding-bottom: 0.5em;
 }
@media only screen and (max-width: 576px) {
  .header__links {
    display: none;
  }
  
}
@media only screen and (max-width: 1090px) {
  .header__links{
    display: none;
  }
}
</style>
