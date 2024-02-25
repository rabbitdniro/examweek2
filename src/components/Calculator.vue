<script setup>
import { ref } from 'vue';

const num1 = ref("");
const num2 = ref("");
const sign = ref("Select Operation");

let result = ref("");

function calculate() {
    
    if (sign.value == "Select Operation") {
        alert("Select Operation");
    }

    try {
        num1.value = Number(num1.value);
    } catch (error) {
        alert("Enter Number");
    }

    try {
        num2.value = Number(num2.value);
    } catch (error) {
        alert("Enter Number");
    }
    
    switch(sign.value) {
        case "add":
            result.value = num1.value + num2.value;
            break;
        case "sub":
            result.value = num1.value - num2.value;
            break;
        case "mul":
            result.value = num1.value * num2.value;
            break;
        case "div":
            result.value = num1.value / num2.value;
            break;
    }
}

function clear() {
    num1.value = "";
    num2.value = "";
    sign.value = "Select Operation";
    result.value = "";
}
</script>

<template>
    <div class="container">
        <div>
            <h1>Calculator</h1>
        </div>
        
        <div class="row mt-5">
            <div class="col">
                <div class="input-group">
                    <span class="input-group-text">First Num</span>
                    <input v-model.number="num1" id="num1" class="form-control" placeholder="Enter Number">
                </div>
            </div>
            <div class="col">
                <div class="input-group">
                    <span class="input-group-text">Second Num</span>
                    <input v-model.number="num2" id="num2" class="form-control" placeholder="Enter Number">
                </div>
            </div>
            <div class="col">
                <div class="input-group">
                    <select v-model="sign" class="form-select">
                        <option selected disabled value="Select Operation">Select Operations</option>
                        <option value="add">Addition (+)</option>
                        <option value="sub">Subtraction (-)</option>
                        <option value="mul">Multiplication (*)</option>
                        <option value="div">Division (/)</option>
                    </select>
                </div>
            </div>
        </div>

        <div class="row mt-5">
            <div class="col">
                <button @click="calculate()" type="button" class="btn btn-outline-primary">Calculate</button>
            </div>

            <div class="col">
                <button @click="clear()" type="button" class="btn btn-outline-primary">Clear</button>
            </div>
        </div>

        <div class="row mt-5">
            <div class="col">
                <span>
                    Result: {{ result }}
                </span>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>