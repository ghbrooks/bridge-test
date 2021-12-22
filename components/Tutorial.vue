<template>
  <div class="outer">
    <div class="outer-blur-layer">
    <div class="inner">
      <h1>Calculating your total costs</h1>
      <div class="cost-variable">
        <btn class="cost-variable-item" @click="addValueToTotal(6.00)">
          <img src="~assets/images/tick.svg" />
          <p>Identify requirments</p>
          <p class="cost-variable-item_estimate-text">
            <span>Estimate</span>
            </br><span> £6.00 </span>
          </p>
        </btn>
        <btn class="cost-variable-item" @click="addValueToTotal(3.00)">
          <img src="~assets/images/tick.svg" />
          <p>Identify requirments</p>
          <p class="cost-variable-item_estimate-text">
            <span>Estimate</span>
            </br><span> £3.00 </span>
          </p>
        </btn>
        <btn class="cost-variable-item" @click="addValueToTotal(16.00)">
          <img src="~assets/images/tick.svg" />
          <p>Identify requirments</p>
          <p class="cost-variable-item_estimate-text">
            <span>Estimate</span>
            </br><span> £16.00 </span>
          </p>
        </btn>
        <btn class="cost-variable-item" @click="addValueToTotal(6.00)">
          <img src="~assets/images/tick.svg" />
          <p>Identify requirments</p>
          <p class="cost-variable-item_estimate-text">
            <span>Estimate</span>
            </br><span> £6.00 </span>
          </p>
        </btn>
        <btn class="cost-variable-item" @click="addValueToTotal(21.55)">
          <img src="~assets/images/tick.svg" />
          <p>Identify requirments</p>
          <p class="cost-variable-item_estimate-text">
            <span>Estimate</span>
            </br><span> £21.55 </span>
          </p>
        </btn>
        <btn class="cost-variable-item" @click="addValueToTotal(13.00)">
          <img src="~assets/images/tick.svg" />
          <p>Identify requirments</p>
          <p class="cost-variable-item_estimate-text">
            <span>Estimate</span>
            </br><span> £13.00 </span>
          </p>
        </btn>
        <btn class="cost-variable-item" @click="addValueToTotal(4.30)">
          <img src="~assets/images/tick.svg" />
          <p>Identify requirments</p>
          <p class="cost-variable-item_estimate-text">
            <span>Estimate</span>
            </br><span> £4.30 </span>
          </p>
        </btn>
        <btn class="cost-variable-item" @click="addValueToTotal(6.00)">
          <img src="~assets/images/tick.svg" />
          <p>Identify requirments</p>
          <p class="cost-variable-item_estimate-text">
            <span>Estimate</span>
            </br><span> £6.00 </span>
          </p>
        </btn>
        <btn class="cost-variable-item" @click="addValueToTotal(6.50)">
          <img src="~assets/images/tick.svg" />
          <p>Identify requirments</p>
          <p class="cost-variable-item_estimate-text">
            <span>Estimate</span>
            </br><span> £6.50 </span>
          </p>
        </btn>

        <li class="cost-variable-item">
          <p>Total</p>
          <p>£{{ count.toFixed(2) }}</p>
        </li>
      </div>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
return {
    count: 0,
    addedValue: true
  };
},
  methods: {
    addValueToTotal (value) {
      if (this.addedValue === true) {
        this.count += value;
        this.addedValue = false
      } else if (this.addedValue === false) {
        this.count -= value;
        this.addedValue = true
      }
    }
  }
}
</script>