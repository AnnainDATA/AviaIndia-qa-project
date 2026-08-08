✈️ AviaIndia — Discount Generator QA Documentation
Welcome to the AviaIndia project repository! 
This project covers the full QA testing lifecycle for the flight ticket discount calculation logic for destinations in India and Asia.

Here you will find technical specifications, test design techniques, test scenarios, and detailed test cases.

📁 Quick Links to Repository Files
📋 Task_AviaIndia.pdf — Technical Task and original business requirements for discount calculation[cite: 3].

📊 Decision_table_AviaIndia.pdf — Decision Table covering all condition combinations[cite: 1].

🗺️ Scenario_AviaIndia.pdf — Test Scenarios: positive, negative, and navigation checks[cite: 2].

🧪 Test_design_AviaIndia.pdf — Test Design & Test Cases with steps and expected results[cite: 4].

📌 Business Logic Overview (Business Rules)
The airline offers discounts on regular air travel under specific conditions (according to Task_AviaIndia.pdf):

Age Categories:

👶 0 – 2 years: 100% discount (travels for free)[cite: 3].

🧒 2.1 – 18 years: 40% discount for all destinations[cite: 3].

🧑 18+ years: Base discount depends on the destination and day of departure[cite: 3].

Rules for Passengers Over 18 Years Old:

Destinations in India: 20% discount, provided departure is NOT on Monday or Friday[cite: 3].

Destinations outside India (Asia): 25% discount, provided departure is NOT on Monday or Friday[cite: 3].

Length of Stay: Passengers staying at least 6 days at their destination receive an additional 10% discount[cite: 3].

🛠️ Test Documentation Structure
1. Decision Table
To analyze all logical combinations (age, destination, departure days, trip duration), a Decision Table was compiled[cite: 1]. It allowed us to minimize the number of test cases while maintaining 100% coverage for both round trips and one-way trips (One way trip)[cite: 1].

2. Test Scenarios
Scenarios are categorized in Scenario_AviaIndia.pdf as follows[cite: 2]:

Positive Scenarios: Generation of all valid discount rates (0%, 10%, 20%, 25%, 30%, 35%, 40%, 100%) and purchasing one-way tickets[cite: 2].

Negative Scenarios: Validation of empty required fields (Date of birth, Departure place, Arrival place, Dates) and invalid date entries (e.g., Return date earlier than Departure date)[cite: 2].

Navigation / Transitions: Page navigation and returning to the main page[cite: 2].

3. Test Cases
The complete suite of test cases is detailed in Test_design_AviaIndia.pdf[cite: 4]. Each test case includes:

Preconditions[cite: 4]

Steps to reproduce[cite: 4]

Expected Results[cite: 4]
