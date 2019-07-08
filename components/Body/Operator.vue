<template>
    <div class="operator-container">
        <h2>Tersedia Berbagai Pilihan Operator</h2>
        <h3>Cukup masukkan nomor handphone, sistem kami akan mendeteksi operator seluler secara otomatis</h3>
        <ul class="operator-list">
            <li v-for="operator in operatorImg" :key="operator.id">
                <a v-bind:href="operator.link">
                    <img v-bind:src="operator.img" />
                </a>
            </li>
        </ul>
    </div>
</template>

<script>

export default {
    name: 'Operator',
    data() {
        return{
            operatorImg: [
                {
                    id: 1,
                    img: "https://s1.blanja.com/desktop/images/microsite/img-telkomsel.png",
                    link: "https://www.blanja.com/top-up/paket-data/telkomsel"
                },
                {
                    id: 2,
                    img: "https://s1.blanja.com/desktop/images/microsite/img-indosat.png",
                    link: "https://www.blanja.com/top-up/paket-data/indosat"
                },
                {
                    id: 3,
                    img: "https://s1.blanja.com/desktop/images/microsite/img-xl.png",
                    link: "https://www.blanja.com/top-up/paket-data/xl"
                },
                {
                    id: 4,
                    img: "https://s1.blanja.com/desktop/images/microsite/img-tri.png",
                    link: "https://www.blanja.com/top-up/paket-data/tri"
                },
                {
                    id: 5,
                    img: "https://s1.blanja.com/desktop/images/microsite/img-axis.png",
                    link: "https://www.blanja.com/top-up/paket-data/axis"
                },
                {
                    id: 6,
                    img: "https://s1.blanja.com/desktop/images/microsite/img-garuda.png",
                    link: "https://www.blanja.com/top-up/paket-data/garuda"
                },
                {
                    id: 7,
                    img: "https://s1.blanja.com/desktop/images/microsite/img-pln.png",
                    link: "https://www.blanja.com/top-up/paket-data/pln"
                },
                {
                    id: 8,
                    img: "https://s1.blanja.com/desktop/images/microsite/img-telkom.png",
                    link: "https://www.blanja.com/top-up/paket-data/telkom"
                },
            ]
        }
    }
}
</script>


