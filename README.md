Technical Evaluation Write-Up
GitHub Repository Link
Data-Driven Testing with Playwright

Challenges and Solutions
Navigating the Asana UI:

Challenge: Asana's interface dynamically loads elements, making it difficult to interact with elements directly after navigation.
Solution: Implemented waitForSelector to ensure elements are loaded before interacting. Used Playwright's robust handling of dynamic content to wait for necessary elements to appear.
Dynamic Locators:

Challenge: Generating dynamic locators based on JSON data required a flexible approach to selector creation.
Solution: Utilized template literals to dynamically create selectors. This allowed us to navigate and verify elements based on varying input data.
Handling Asynchronous Operations:

Challenge: Ensuring all steps within a test case execute in the correct sequence.
Solution: Used async/await syntax extensively to manage asynchronous operations, ensuring each step completes before the next begins.
Recommendations
Enhanced Error Logging:

Implement detailed error logging within each test step. This will help in quickly identifying which step failed and why, especially useful for data-driven tests where multiple test cases are executed in sequence.
Improved Element Selectors:

Use more robust and unique selectors for navigating the UI. This can include ARIA roles or data attributes provided by Asana, which are less likely to change than CSS classes or element hierarchies.
Test Coverage:

Expand test coverage to include additional UI interactions beyond navigation and verification. For example, tests could include creating new tasks, updating task statuses, and verifying changes persist across sessions.
Parameterized Testing:

Utilize Playwright’s ability to run parameterized tests to cover various user scenarios and data sets without duplicating test code.
Modularize Test Code:

Break down test steps into reusable functions. This makes the codebase more maintainable and allows for easier updates if the Asana UI changes.


Instructions to Run the Test
Setup Project:

Clone the repository: git clone https://github.com/manchekke2/playwright-data-driven-test.git
Navigate to the project directory: cd playwright-data-driven-test
Install dependencies: npm install
Run Tests:

Execute the tests using Playwright: npx playwright test
