<script>
export default {
    data: function () {
        return {
            mode: 'AMD_to_USD',
            amount: 0,
            convertedAmount: 0

        };
    },

    methods: {
        convertCurrency() {
            if (this.mode === 'AMD_to_USD') {
                this.convertedAmount = this.amount / 400;
            } else {
                this.convertedAmount = this.amount * 400;
            }
        },
        toggleMode() {
            this.mode = this.mode === 'AMD_to_USD' ? 'USD_to_AMD' : 'AMD_to_USD';
            this.amount = 0;
            this.convertedAmount = 0;
        }
    }


}
</script>

<template>
    <div class="main">
        <h2 v-if="mode === 'AMD_to_USD'">AMD to USD</h2>
        <h2 v-else>USD to AMD</h2>
        <input type="number" 
        :value="amount"
         @input="convertCurrency">

        <span> ➜ </span>

        <input type="number"
         :value="convertedAmount" 
        readonly 
        :disabled="mode === 'USD_to_AMD'">
        <div>
            <button @click="toggleMode">{{ mode === 'AMD_to_USD' ? 'AMD -> USD' : 'USD -> AMD' }}</button>
        </div>

    </div>

</template>


<style scoped>
input {
    border: 3px solid #163611;
    margin: 10px;
    width: 200px;
    height: 50px;

}

h2 {
    color: rgb(11, 11, 14);
    font-weight: 600;
    text-align: center;
}

.main {
    background-color: rgb(36, 186, 31);
    border-radius: 8px;
}
</style>
