<template>
    <div>
        <v-row align="center" justify="center">
            <v-col cols="12">
                <v-card-text :style="{fontFamily: 'Verdana', fontSize: '18px'}">
                    Necesitamos de su colaboración para continuar con el mantenimiento de las unidades de emergencia y dependencias.
                        Adquirir elementos de comunicación, salvamento, material contra incendio, pago de combustible, seguros de vida y automotores, como así también actualizar los elementos de protección personal,
                        dado que estos últimos sufren un gran desgaste. Lamentablemente, no estamos exentos de los servicios básicos, por lo tanto también debemos abonar los servicios luz, gas, internet, telefonía, etc.
                        La misión primordial de Bomberos Voluntarios de Lanús radica en fortalecer la seguridad en la sociedad mientras respalda el valioso compromiso de aquellos individuos que han abrazado la noble vocación de salvaguardar a los demás.
                        Nuestro propósito fundamental es tejer una extensa red de colaboración destinada a prevenir incidentes y ofrecer una respuesta efectiva ante emergencias.
                        En este sentido, dedicamos esfuerzos hacia el bienestar integral de cada bombero, asegurando tanto su salud física como emocional, para que puedan llevar a cabo su labor de manera óptima.
                        Al mismo tiempo, aspiramos a fomentar la participación activa de cada ciudadano en la protección de su comunidad.
                </v-card-text>
            </v-col>
            <v-col cols="12" md="2" v-if="$vuetify.display.mdAndUp">
                <h3>¡Escaneá el QR y doná!</h3>
                <v-img width="200" height="200" cover src="../../assets/qr.png"></v-img>
            </v-col>
            <v-col cols="12" md="3">
                <h2 class="mb-4 text-center">Datos de transacción</h2>
                <v-text-field variant="outlined" label="Alias" readonly :model-value="alias" />
                <v-text-field variant="outlined" label="Nombre" readonly :model-value="name" />
                <v-text-field variant="outlined" label="CBU" readonly :model-value="cbu" />
            </v-col>
            <v-col cols="12">
                <v-form v-model="formValue" ref="form">
                    <v-row align="center" justify="center">
                        <v-col cols="12" md="2" class="text-center">
                            <v-rating
                                v-model="rating"
                                bg-color="red"
                                color="primary"
                            ></v-rating>
                        </v-col>
                        <v-col cols="12" md="4">
                            <v-text-field variant="solo" label="Mensaje de agradecimiento" :rules="messageRule" 
                                v-model="message"></v-text-field>
                        </v-col>
                        <v-col cols="12" md="12" align="center">
                            <v-row align="center" justify="center">
                                <v-col cols="6">
                                    <v-btn color="primary" block :disabled="!formValue">
                                        <v-icon>mdi-send</v-icon>
                                    </v-btn>
                                </v-col>
                            </v-row>
                        </v-col>
                    </v-row>
                </v-form>
            </v-col>
        </v-row>
    </div>
</template>

<script>
    export default {
        name: 'Donations-Component',
        data: () => ({
            alias: 'bomberos.lanus.mp',
            name: 'Bomberos Voluntarios Lanús',
            cbu: '0000003100076208932278',
            rating: 0,
            message: '',
            messageRule: [
                v => !!v || 'Este campo es obligatorio',
                v => v.length < 50 || 'El mensaje debe tener menos de 50 caracteres'
            ],
            formValue: true,
        }),
        mounted(){
            this.$refs.form.validate()
        }
    }
</script>

<style lang="scss" scoped>

</style>