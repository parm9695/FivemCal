<template>
  <v-container>
    <v-row align="center">
      <v-col cols="12" sm="6" md="6" lg="6">
        <v-text-field
        type="number"
          v-model="cement"
          label="ปูน"
          hide-details="auto"
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row align="center">
      <v-col cols="12" sm="6" md="6" lg="6">
        <v-text-field
        type="number"
          v-model="blackMoney"
          label="เงินแดง"
          hide-details="auto"
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row align="center">
      <v-col cols="12" sm="6" md="6" lg="6">
        <v-text-field
          v-model="result"
          label="รวม"
          hide-details="auto"
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" sm="3" md="3" lg="3">
        <v-btn @click="Calculate"> คำนวน </v-btn>
      </v-col>
      <v-col cols="12" sm="3" md="3" lg="3">
        <v-btn @click="reset"> Reset </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    cement: 0,
    blackMoney: 0,
    result : 0,
  }),
  methods:{
    Calculate(){
      const calCement = parseInt(this.cement) * 500
      const calBlackMoney = parseInt(this.blackMoney) * 2
      this.result = parseInt(calCement)  + parseInt(calBlackMoney)
    },
    reset(){
      this.cement = 0
      this.blackMoney = 0
      this.result = 0
    }
  }
};
</script>
