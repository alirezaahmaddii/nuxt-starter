<template>
  <div class="drawer">
    <transition name="fade" appear>
      <div
        class="back-shadow"
        v-if="$store.state.theme.drawerIsOpen"
        @click="$store.dispatch('theme/setDrawerStatus', false)"
      ></div>
    </transition>
    <transition name="drawer-pop" appear>
      <div class="box-items" v-if="$store.state.theme.drawerIsOpen">
        <div class="row drawer__box-items__logo-header">
          <div class="col-12 d-flex justify-content-center align-items-center pt-3"
               @click="$store.dispatch('theme/setDrawerStatus', false)">

            <!-- img-logo -->
            <!--<img src="" alt="">-->

          </div>
          <nav>
            <hr/>
            <!--main nav-->
            <ul>
              <li @click="$store.dispatch('setDrawerStatus', false)">
                <nuxt-link to="/">...</nuxt-link>
              </li>
              <li><br/><br/><br/><br/></li>
            </ul>
          </nav>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: "site-drawer",
};
</script>

