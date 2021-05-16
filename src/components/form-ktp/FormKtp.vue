<template>
    <v-card>
        <v-card-title>
            <h2>Silahkan Input / Scan KTP Anda</h2>
        </v-card-title>
        <v-form ref="form" v-model="valid" lazy-validation>
            <v-col class="col-11 ml-5 mr-5">
                <v-text-field v-model="idktp" :counter="16" :rules="idRules" label="No. KTP" required></v-text-field>
            </v-col>                
            <v-col class="col-11 ml-5 mr-5">
                <v-text-field v-model="name"  :rules="nameRules" label="Nama" required></v-text-field>
            </v-col>
            <v-col class="col-11 ml-5 mr-5">
                <v-text-field v-model="pekerjaan"  label="Pekerjaan" required></v-text-field>            
            </v-col>
            <v-col class="col-11 ml-5 mr-5">
                <v-text-field v-model="alamat"  label="Alamat" required></v-text-field>
            </v-col>
            <v-col class="col-11 ml-5 mr-5">
                <v-text-field v-model="desa"  label="Desa" required></v-text-field>
            </v-col>
            <v-col class="col-11 ml-5 mr-5">
                <v-text-field v-model="kota"  label="Kota" required></v-text-field>    
            </v-col>            
            <v-col class="col-11 ml-5 mr-5">
                <v-btn :disabled="!valid" color="success" class="mr-4" @click="validate">
                    Validate
                </v-btn>

                <v-btn color="error" class="mr-4" @click="reset">
                Reset Form
                </v-btn>
            </v-col>
        </v-form>
    </v-card>
</template>
<script>
export default {
    data: () => ({
      valid: true,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 50) || 'Name must be less than 50 characters',
      ],
      idktp: '',
      idRules: [
        v => !!v || 'NIK is required',
        v => (v && v.length <= 16) || 'NIK must be less than 16 characters',
      ],
      pekerjaan: '',
      alamat: '',
      desa: '',
      kota: ''
    }),
    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      },
    },
  }
</script>
