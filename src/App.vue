<template>
  <div id="app">
    <div class="header">
      <div class="totalSavings">
        <h2>Total Savings</h2>
        <p>$7,467.25</p>
      </div>
    </div>

    <div class="input"></div>

    <div class="transactions">
      <div class="wrapper">
        <div class="income">
          <div class="totalIncome">
            <h2>Total Income</h2>
            <p>$9,148.20</p>
          </div>
          <div class="transactionList">
            <ul>
              <li>Transaction 1</li>
              <li>Transaction 2</li>
              <li>Transaction 1</li>
            </ul>
          </div>
        </div>

        <div class="expenses">
          <div class="totalExpenses">
            <h2>Total Expenses</h2>
            <p>$1,680.96</p>
          </div>
          <div class="expenseTransactions">
            <div class="transactionList">
              <ul>
                <li>Transaction 1</li>
                <li>Transaction 2</li>
                <li>Transaction 1</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {};
  },
  methods: {}
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #f5f5f5;
  font-family: "Roboto", sans-serif;
}

.wrapper {
  max-width: 870px;
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
}

.header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 250px;
  background-image: linear-gradient(#3827b4, hsla(276, 74%, 37%, 0.6));
  color: #fff;
}

.totalSavings {
  text-align: center;
}

.totalSavings h2 {
  font-size: 20px;
  color: rgba(255, 255, 255, 0.7);
}

.totalSavings p {
  font-size: 40px;
}

.transactions {
  padding-top: 40px;
}

.income,
.expenses {
  width: 405px;
}

.totalIncome,
.totalExpenses {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 90px;
  color: #fff;
  border-radius: 20px;
  box-shadow: 0 30px 40px rgba(0, 0, 0, 0.08);
}

.totalIncome {
  background-color: #813baf;
}

.totalExpenses {
  background-color: #5544cc;
}

.totalIncome h2,
.totalExpenses h2 {
  font-size: 18px;
  color: rgba(255, 255, 255, 0.7);
}

.totalIncome p,
.totalExpenses p {
  font-size: 25px;
}

.transactionList {
  background-color: #fff;
  border-radius: 20px;
  margin-top: 22px;
  box-shadow: 0 30px 40px rgba(0, 0, 0, 0.08);
  padding: 22px;
}

.transactionList ul {
  list-style: none;
}
</style>
