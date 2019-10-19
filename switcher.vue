<template>
    <div>
        <label class="switch">
            <input type="checkbox" v-model="valueCheck"/>
            <div class="slider round"></div>
        </label>
    </div>
</template>
<script>

export default {

    name: 'switcher',
    props:['value'],
    data(){

      return{

        valueCheck: this.value,

      }

    },
    watch:{

      value(){

        this.valueCheck= this.value

      },

      valueCheck(val){

        this.$emit('input', val)

      }

    }

}

</script>
<style scoped>

.switch {
  display: inline-block;
  height: 15px;
  position: relative;
  width: 40px;
}

.switch input {
  display:none;
}

.slider {
  display:flex;
  align-items: center;
  background-color: #ccc;
  bottom: 0;
  cursor: pointer;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  transition: .2s;
}

.slider:before {
  content: "";
  position: absolute;
  width: 18px;
  height: 18px;
  transition: .2s;
  background-color: #fff;
}

input:checked + .slider {
  background-color: #66bb6a;
}

input:checked + .slider:before {
  transform: translateX(22px);
}

.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}

</style>