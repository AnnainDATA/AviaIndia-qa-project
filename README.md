# ✈️ AviaIndia — Discount Generator QA Documentation

Welcome to the **AviaIndia** project repository! 
This project covers the full QA testing lifecycle for the flight ticket discount calculation logic for destinations in India and Asia.

Here you will find technical specifications, test design techniques, test scenarios, and detailed test cases.

---

## 📁 Quick Links to Repository Files

* 📋 [Task_AviaIndia.pdf](./Task_AviaIndia.pdf) — **Technical Task** and original business requirements for discount calculation.
* 📊 [Decision_table_AviaIndia.pdf](./Decision_table_AviaIndia.pdf) — **Decision Table** covering all condition combinations.
* 🗺️ [Scenario_AviaIndia.pdf](./Scenario_AviaIndia.pdf) — **Test Scenarios**: positive, negative, and navigation checks.
* 🧪 [Test_design_AviaIndia.pdf](./Test_design_AviaIndia.pdf) — **Test Design & Test Cases** with steps and expected results.

---

## 📌 Business Logic Overview (Business Rules)

The airline offers discounts on regular air travel under specific conditions (according to [Task_AviaIndia.pdf](./Task_AviaIndia.pdf)):

1. **Age Categories:**
   * 👶 **0 – 2 years:** **100%** discount (travels for free).
   * 🧒 **2.1 – 18 years:** **40%** discount for all destinations.
   * 🧑 **18+ years:** Base discount depends on the destination and day of departure.

2. **Rules for Passengers Over 18 Years Old:**
   * **Destinations in India:** **20%** discount, provided departure is **NOT** on Monday or Friday.
   * **Destinations outside India (Asia):** **25%** discount, provided departure is **NOT** on Monday or Friday.
   * **Length of Stay:** Passengers staying **at least 6 days** at their destination receive an **additional 10%** discount.

---

## 🛠️ Test Documentation Structure

### 1. Decision Table
To analyze all logical combinations (age, destination, departure days, trip duration), a [Decision Table](./Decision_table_AviaIndia.pdf) was compiled. It allowed us to minimize the number of test cases while maintaining 100% coverage for both round trips and one-way trips (`One way trip`).

### 2. Test Scenarios
Scenarios are categorized in [Scenario_AviaIndia.pdf](./Scenario_AviaIndia.pdf) as follows:
* **Positive Scenarios:** Generation of all valid discount rates (0%, 10%, 20%, 25%, 30%, 35%, 40%, 100%) and purchasing one-way tickets.
* **Negative Scenarios:** Validation of empty required fields (Date of birth, Departure place, Arrival place, Dates) and invalid date entries (e.g., Return date earlier than Departure date).
* **Navigation / Transitions:** Page navigation and returning to the main page.

### 3. Test Cases
The complete suite of test cases is detailed in [Test_design_AviaIndia.pdf](./Test_design_AviaIndia.pdf). Each test case includes:
* Preconditions
* Steps to reproduce
* Expected Results
