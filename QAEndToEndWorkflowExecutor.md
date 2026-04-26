# Agentic QA Workflow Prompt

## 🎯 Objective

Execute an end-to-end QA workflow for the user story:
**"Search and Add Highly Rated Product to Cart"**

---

## 📥 Input

* User Story File Path:
  `userStories/Jira_1245-34567_findGoodRatingProduct.md`

---

## 🧠 Step 1: Test Planning (Playwright Test Planner Agent)

### Instructions:

1. Read and analyze the user story from the given file path.

2. Identify:

   * Functional requirements
   * Acceptance criteria
   * User flows
   * Risk areas (high defect probability zones)

3. Generate **comprehensive exploratory test cases**.

### Coverage Requirements:

* ✅ Positive scenarios
* ✅ Negative scenarios
* ✅ Edge cases
* ✅ Boundary conditions
* ✅ High defect density areas:

  * Search functionality
  * Filters (ratings, price, category)
  * Sorting logic
  * Add to cart behavior
  * Session/cart persistence

### Test Case Format:

Each test case must include:

* **Test Case ID**
* **Title**
* **Description**
* **Preconditions**
* **Test Steps**
* **Test Data**
* **Expected Result**
* **Actual Result (initially empty)**

### Output:

* Save test cases in:
  `specs/search_add_high_rating_product.spec.md`

---

## 🔍 Step 2: Manual Exploratory Execution (Playwright MCP Agent)

### Instructions:

1. Execute all test cases from `specs` folder using MCP tools.
2. Simulate real user behavior.

### Execution Requirements:

* Capture **screenshots**:

  * At key steps
  * On failures
* Record:

  * Actual Results
  * Observations
  * Defects (if any)

### Output:

* Update test cases with:

  * Actual Results
  * Pass/Fail Status
* Save execution log:
  `specs/execution-results.md`
* Store screenshots:
  `specs/screenshots/`

---

## 🤖 Step 3: Automation Script Generation (Playwright Automation Agent)

### Instructions:

1. Read:

   * Test cases from `specs`
   * Execution results

2. Generate Playwright automation scripts.

### Coding Standards:

* Use **stable locators**:

  * ID
  * Name
  * CSS selectors
  * LinkText
* Use:

  * Explicit waits
  * Assertions
  * Reusable functions
* Naming:

  * Function names = Test Case Titles

### Output:

* Save scripts in:
  `tests/automated-tests/`

---

## 🛠 Step 4: Automation Execution & Healing (Playwright Healer Agent)

### Instructions:

1. Execute all automation scripts.
2. Identify failed tests.

### Healing Process:

For each failed test:

* Analyze failure reason:

  * Locator issue
  * Timing issue
  * Assertion failure
* Fix using:

  * Better locator strategy
  * Wait adjustments
  * Assertion correction

### Loop:

Repeat execution + healing until:
✅ All tests pass and are stable

### Output:

* Initial execution report
* Healing logs:

  * Issue identified
  * Fix applied
* Final execution status

Save in:
`tests/automation-execution-report/`

---

## 📊 Step 5: Final Report Generation (Reporting Agent)

### Instructions:

Combine:

* Manual exploratory results
* Automation execution results

### Report Should Include:

* Test coverage summary
* Total test cases
* Pass/Fail metrics
* Defects identified
* Flaky tests (if any)
* Healing insights
* Screenshots reference
* Recommendations

### Output:

`final-report/qa-summary-report.md`

---

## 🚀 Step 6: Git Integration (Git Agent)

### Instructions:

1. Initialize git repository (if not already)
2. Commit all changes
3. Push to remote
4. Create Pull Request

### Output:

* Repository URL
* PR Link
