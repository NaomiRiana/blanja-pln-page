<template>
    <div>
        <div class="options">
            <div class="option">
                <label>
                    <input v-model="selectedRadio" type="radio" name="radio" value="token" checked="checked" />
                    <span class="radio-box"></span>
                    Token Listrik
                </label>
            </div>
            <div class="option">
                <label>
                    <input v-model="selectedRadio" type="radio" name="radio" value="tagihan" />
                    <span class="radio-box"></span>
                    Tagihan Listrik
                </label>
            </div>
        </div>
        <div class="number-input">
            <label for="input-no">No. Meter/ID Pelanggan</label>
            <div class="number-input-area">
                <input id="input-no" type="tel" placeholder="Contoh 1122-3344-5555">
                <span class="logo-pln-area">
                    <img class="logo-pln" src="//s1.blanja.com/desktop/images/microsite/logo-pln-b.png" alt="PLN">
                </span>
            </div>
        </div>
        <transition name="token-nominal">
            <div v-if="selectedRadio==='token'" class="nominal-input">
                <label for="input-nominal">Nominal</label>
                <div  class="nominal-box-wrapper">
                    <div v-bind:class="{ 'nominal-box active': (selectedNom===nominal) }" 
                        class="nominal-box" 
                        v-for="nominal in nominals" 
                        @click="priceDisplay(nominal)"
                        :key="nominal.id">
                        Rp {{nominal.price}}
                    </div>
                </div>
            </div>
        </transition>
        <div class="pln-action-notif">
            <div class="pln-notif">
                <span class="pln-notif-icon-area">
                    <img src="//s1.blanja.com/desktop/images/microsite/info@2x.png">
                </span>
                <p>Transaksi Token PLN <b>pukul 23:00 - 00:59 WIB</b> akan diproses setelah <b>pukul 01:00 WIB</b></p>
            </div>
        </div>
        <button type="button" class="pln-action-button" >Blanja Token Listrik</button>
        <p class="price">Harga
            <span class="selected-price">{{ selectedNom.price }}</span>
        </p>
    </div>
</template>

<script>
export default {
  data(){
        return{
            // currentPrice: this.nominals[0],
            selectedRadio:'token',            
            nominals: [
                {
                    id:'1',
                    price:'20.000'
                },
                {
                    id:'2',
                    price:'50.000'
                },
                {
                    id:'3',
                    price:'100.000'
                },
                {
                    id:'4',
                    price:'200.000'
                },
                {
                    id:'5',
                    price:'500.000'
                },
                {
                    id:'6',
                    price:'1.000.000'
                },
                {
                    id:'7',
                    price:'5.000.000'
                },
                {
                    id:'8',
                    price:'10.000.000'
                },
                {
                    id:'9',
                    price:'50.000.000'
                },
            ],
            selectedNom: {
                    id:'1',
                    price:'20.000'
                },
        }
        console.log(this.nominals);
        
    },

    methods: {
        priceDisplay(nomPrice){
            this.selectedNom=nomPrice;
        }
    },
}
</script>
