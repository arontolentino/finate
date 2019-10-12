<template>
  <div id="app">
    <div class="header">
      <div class="totalSavings">
        <h2>Total Savings</h2>
        <p>$7,467.25</p>
      </div>
      <div class="input">
        <div class="wrapper">
          <div class="inputContainer">
            <input
              placeholder="Date"
              class="textbox-n"
              type="text"
              onfocus="(this.type='date')"
              id="date"
            />
          </div>
          <div class="inputContainer">
            <input type="text" placeholder="Description" />
          </div>

          <div class="inputContainer">
            <select>
              <option disabled selected>Transaction Type</option>
              <option>Income</option>
              <option>Expense</option>
            </select>
          </div>

          <div class="inputContainer">
            <input type="number" placeholder="Amount" />
          </div>
        </div>
      </div>
    </div>

    <div class="transactions">
      <div class="wrapper">
        <div class="income">
          <div class="totalIncome">
            <h2>Total Income</h2>
            <p>$9,148.20</p>
          </div>
          <div class="transactionList">
            <ul>
              <li v-for="(income, index) in incomeList" :key="index">
                <div class="icon">{{ income.icon }}</div>
                <div class="description">
                  <div class="date">{{ income.date }}</div>
                  <div class="name">{{ income.desc }}</div>
                </div>
                <div class="amount">${{ income.amount }}</div>
              </li>
            </ul>
          </div>
        </div>

        <div class="expenses">
          <div class="totalExpenses">
            <h2>Total Expenses</h2>
            <p>$1,680.96</p>
          </div>

          <div class="transactionList">
            <ul>
              <li v-for="(income, index) in incomeList" :key="index">
                <div class="icon">{{ income.icon }}</div>
                <div class="description">
                  <div class="date">{{ income.date }}</div>
                  <div class="name">{{ income.desc }}</div>
                </div>
                <div class="amount">-${{ income.amount }}</div>
              </li>
            </ul>
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
    return {
      incomeList: [
        {
          icon: "Icon",
          date: "October 4, 2019",
          desc: "Item 1",
          amount: 132.94
        },
        {
          icon: "Icon",
          date: "October 5, 2019",
          desc: "Item 2",
          amount: 183.29
        },
        {
          icon: "Icon",
          date: "October 6, 2019",
          desc: "Item 3",
          amount: 302.12
        }
      ],
      expenseList: [
        {
          icon: "Icon",
          date: "October 4, 2019",
          desc: "Item 1",
          amount: 132.94
        },
        {
          icon: "Icon",
          date: "October 5, 2019",
          desc: "Item 2",
          amount: 183.29
        },
        {
          icon: "Icon",
          date: "October 6, 2019",
          desc: "Item 3",
          amount: 302.12
        }
      ]
    };
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
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 300px;
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

.input {
  position: absolute;
  bottom: -40px;
  width: 870px;
  border-radius: 20px;
  height: 80px;
  background-color: #fff;
  box-shadow: 0 30px 40px rgba(0, 0, 0, 0.08);
  padding: 24px 45px;
}

.inputContainer {
  padding: 3px;
  border-bottom: 1px solid #e6e6e6;
}

input,
select {
  font-family: "Roboto", sans-serif;
  font-size: 15px;
  border: none;
  color: #a3a2ac;
}

::placeholder {
  color: #a3a2ac;
}

input:focus,
select:focus {
  outline: none;
}

select {
  background-color: #fff;
}

.transactions {
  padding-top: 77px;
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
  padding: 7.5px 22px;
}

.transactionList ul {
  list-style: none;
}

.transactionList li:not(:last-child) {
  border-bottom: 1px solid #e6e6e6;
}

.transactionList li {
  display: flex;
  justify-content: space-between;
  padding: 17.5px 10px;
  font-weight: 300;
}

.icon {
  width: 10%;
}

.description {
  width: 55%;
}

.name {
  color: #a3a2ac;
}

.amount {
  width: 20%;
  text-align: right;
}

.income .amount {
  color: #3827b4;
}

.expenses .amount {
  color: #e61ead;
}
</style>
