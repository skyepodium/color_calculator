<template>
  <div class="back">
    <div class="wrapper">
      <input
        v-model="inputText"
        type="text"
        class="number"
        readonly
      >
      <div class="pad_wrapper">
        <div class="pad_line">
          <div
            class="box box_2 clear top"
            @click="clear"
          >
            c
          </div>
          <div
            class="box box_1 top"
            @click="clickBox('/')"
          >
            /
          </div>
          <div
            class="box box_1 top"
            @click="clickBox('%')"
          >
            %
          </div>
        </div>
        <div class="pad_line">
          <div
            class="box box_1"
            @click="clickBox('7')"
          >
            7
          </div>
          <div
            class="box box_1"
            @click="clickBox('8')"
          >
            8
          </div>
          <div
            class="box box_1"
            @click="clickBox('9')"
          >
            9
          </div>
          <div
            class="box box_1"
            @click="clickBox('*')"
          >
            *
          </div>
        </div>
        <div class="pad_line">
          <div
            class="box box_1"
            @click="clickBox('4')"
          >
            4
          </div>
          <div
            class="box box_1"
            @click="clickBox('5')"
          >
            5
          </div>
          <div
            class="box box_1"
            @click="clickBox('6')"
          >
            6
          </div>
          <div
            class="box box_1"
            @click="clickBox('-')"
          >
            -
          </div>
        </div>
        <div class="pad_line">
          <div
            class="box box_1"
            @click="clickBox('1')"
          >
            1
          </div>
          <div
            class="box box_1"
            @click="clickBox('2')"
          >
            2
          </div>
          <div
            class="box box_1"
            @click="clickBox('3')"
          >
            3
          </div>
          <div
            class="box box_1"
            @click="clickBox('+')"
          >
            +
          </div>
        </div>  
        <div class="pad_line">
          <div
            class="box box_1"
            @click="clickBox('0')"
          >
            0
          </div>
          <div
            class="box box_1"
            @click="clickBox('00')"
          >
            00
          </div>
          <div
            class="box box_1"
            @click="clickBox('.')"
          >
            .
          </div>
          <div
            class="box box_1 result"
            @click="result"
          >
            =
          </div>
        </div>                
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Calculator',
    data() {
        return {
            inputText: ''
        }
    },
    methods: {
        clear() {
            this.inputText = ""
        },
        clickBox(val) {
            if(!isNaN(val)){
                this.inputText = this.inputText + val
            }
        },
        result() {
            
        }
    }
}
</script>
