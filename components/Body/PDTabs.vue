<template>
    <div class="pd-tab">
        <ul>
            <li v-for="pd in pdList" :key="pd.id">
                <a>
                    <div>
                        <span class="tab-icon" v-bind:id="pd.idCss"></span>
                        <span>{{pd.name}}</span>
                    </div>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'PDTabs',
    data (){
        return{
            pdList: [
                {
                    id:1,
                    name:'Pulsa',
                    idCss: 'pulsa-icon'
                },
                {
                    id:2,
                    name:'Paket Data',
                    idCss: 'paket-data-icon'
                },
                {
                    id:3,
                    name:'Telkom',
                    idCss: 'telkom-icon'
                },
                {
                    id:4,
                    name:'PLN',
                    idCss: 'pln-icon',
                    active:true
                },
                {
                    id:5,
                    name:'Garuda Indonesia',
                    idCss: 'garuda-icon'
                },
                {
                    id:6,
                    name:'BPJS',
                    idCss: 'bpjs-icon'
                },
            ],
        }
    }
}
</script>