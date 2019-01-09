<template>
    <div class="menu1">
        <button
            class="tab"
            v-for="tab in tabs"
            :key="tab"
            :class="['tab-button',{active: currentTab===tab}]"
            @click="clicked(tab)">{{tab}}</button>
    </div>
</template>

<script>
    import {eventBus} from '../app.js';

    export default {
        name: "menuBar",
        data(){
            return {
                currentTab: 'homepage',
                tabs: ['HomePage', 'Project1', 'Project2']
            }
        },

        methods: {
            clicked(tab) {
                this.currentTab = tab;
                console.log(this.currentTab);
                eventBus.$emit('tab-clicked',this.currentTab.toLowerCase());
            }
        }
    }
</script>

<style type="text/scss" lang="scss" scoped>
.menu1{
    display:flex;
    flex-basis: auto;
    flex-grow: 1;
    border: solid 1px #1d68a7;
    margin: auto;
      .tab{
          display: flex;
          position: center;
          font-size: 1rem;
          font-weight: 400;
          margin-right:30px;
          line-height: 1.5;
          margin: auto;
      }
}
</style>
