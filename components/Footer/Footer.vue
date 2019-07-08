<template>
    <div>
        <div class="footer-container">
            <h3 class="footer-title">Jaminan Belanja di Blanja</h3>
            <ul class="jaminan-list">
                <li v-for="jaminan in jaminanList" :key="jaminan.id">
                    <div>
                        <img v-bind:src="jaminan.img" />
                    </div>
                    <span>{{jaminan.capt}}</span>
                </li>
            </ul>
        </div>
        <div class="footer-container">
            <h3 class="footer-title">Berbelanja di blanja Aman</h3>
            <img src="//s1.blanja.com/commons/images/common/icon_security.png">
            <div class="contacts-list">
                <a href="">
                    <i class="bl-headphone"></i>
                    <span>021 - 8066 7878</span>
                </a>
                <a href="">
                    <i class="bl-mail"></i>
                    <span>support@blanja.com</span>
                </a>
                <a href="">
                    <i class="bl-chat"></i>
                    <span>Live Support</span>
                </a>
            </div>
        </div>
        <div class="copyright">            
		    Copyright 2019 © MetraPlasa. All Rights Reserved.
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return{
            jaminanList: [
                {
                    id:"1",
                    img:"https://s1.blanja.com/commons/images/common/ic-pembayaranaman.png",
                    capt:"Pembayaran Aman"
                },
                {
                    id:"2",
                    img:"https://s1.blanja.com/commons/images/common/ic-jaminanpenembalian.png",
                    capt:"Jaminan Pengembalian Dana"
                },
                {
                    id:"3",
                    img:"https://s1.blanja.com/commons/images/common/ic-perlindunganpembeli.png",
                    capt:"Perlindungan Pembeli 100%"
                },
                {
                    id:"4",
                    img:"https://s1.blanja.com/commons/images/common/ic-jaminankepuasan.png",
                    capt:"Jaminan Kepuasan"
                },
            ] 
        }
    }
}
</script>
