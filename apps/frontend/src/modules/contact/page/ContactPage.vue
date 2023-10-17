<template>
    <v-card height="100%">
        <v-card-text>
            <contact-component :items="items" />
        </v-card-text>
        
    </v-card>
</template>

<script>
import ContactComponent from '../components/ContactComponent.vue'

export default {
    name: 'ContactPage',
    components: {
        ContactComponent
    },
    data(){
        return {
            items: [
                {
                    elevation: '2',
                    title: "Cuartel Central",
                    subtitle: "Av. Pres. Raúl Alfonsín 1039, B1825 Gerli, Provincia de Buenos Aires",
                    googlemaps: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3280.264229238027!2d-58.383737023455375!3d-34.698514872920455!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x95bccd28465ce561%3A0x4a2c44eccfcb5756!2sBOMBEROS%20VOLUNTARIOS%20DE%20LAN%C3%9AS!5e0!3m2!1ses!2sar!4v1692458468430!5m2!1ses!2sar"
                },
                {
                    elevation: '2',
                    title: "Destacamento N°1",
                    subtitle: "Matanza 2798-2700, B1825 Monte Chingolo, Provincia de Buenos Aires",
                    googlemaps: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1639.452876012356!2d-58.37112816455339!3d-34.73276996432413!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x95a332aa9bccb7f7%3A0x8bc37510b1923f80!2sBomberos%20De%20Monte%20Chingolo!5e0!3m2!1ses!2sar!4v1694822230804!5m2!1ses!2sar"
                },
                {
                    elevation: '2',
                    title: "Destacamento N°2",
                    subtitle: "Tte. Cnel. Bueras 4355, B1825CRC Monte Chingolo, Provincia de Buenos Aires",
                    googlemaps: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1639.6878112520806!2d-58.346072061083774!3d-34.720925147061166!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x95a332993bda624b%3A0x9fe28a631a96c8a5!2sDestacamento%20N%C2%B02!5e0!3m2!1ses!2sar!4v1694822122101!5m2!1ses!2sar"
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>