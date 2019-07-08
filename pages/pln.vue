<template>
    <div>
        <div class="page-container">
            <PDTabs />
            <div class="page-wrapper">
                <Pln />
            </div>
        </div>
        <div id="operator-container" class="page-container">
            <Operator />
        </div>
        <div v-for="paragraph in paragraphList" :key="paragraph.id">
            <Paragraph v-bind:paragraph="paragraph" />
        </div>
    </div>
</template>

<script>
import axios from 'axios'
import PDTabs from "~/components/Body/PDTabs"
import Pln from "~/components/Body/Pln"
import Operator from "~/components/Body/Operator"
import Paragraph from "~/components/Body/Paragraph"

export default {
    components: {
        PDTabs, Pln, Operator, Paragraph
    },
    data(){
        return{
            paragraphList : []
        }
    },

    mounted() {
        axios.get('http://localhost:3001/paragraphs')
        .then(response => {
            console.log('1',response.data);
            this.paragraphList = response.data
      })
    },
}
</script>


<style lang="scss" scoped>
   @import '../assets/css/style.scss';
</style>