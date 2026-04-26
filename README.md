# Demo

QA End-to-End Workflow with Playwright - Demo project for automated testing using Playwright agents and MCP tools.

## Project Structure

```
├── package.json              # NPM configuration
├── playwright.config.ts      # Playwright configuration
├── QAEndToEndWorkflowExecutor.md  # Workflow instructions
├── specs/                    # Test specifications
│   ├── search_add_high_rating_product.spec.md
│   ├── execution-results.md
│   └── screenshots/
├── tests/                    # Test automation scripts
│   ├── automated-tests/
│   │   ├── search_functionality.spec.ts
│   │   ├── filtering.spec.ts
│   │   ├── product_details.spec.ts
│   │   ├── add_to_cart.spec.ts
│   │   ├── session_e2e.spec.ts
│   │   └── negative_edge_cases.spec.ts
│   ├── seed.spec.ts
│   └── example.spec.ts
├── userStories/              # User story files
│   └── Jira_1245-34567_findGoodRatingProduct.md
├── test-results/             # Test execution results
└── docs/                     # Documentation
    └── qa-workflow.drawio    # Workflow diagram
```

## Workflow Steps

1. **Test Planning** - Generate test cases using Playwright Test Planner Agent
2. **Manual Exploratory** - Execute tests using MCP tools
3. **Automation Scripts** - Generate Playwright automation scripts
4. **Execution & Healing** - Run and fix failing tests
5. **Final Report** - Create QA summary report
6. **Git Integration** - Commit and push changes

## Test Coverage

- Search Functionality (4 tests)
- Product Quality Filtering (4 tests)
- Product Details Validation (4 tests)
- Add to Cart (5 tests)
- Session Handling (3 tests)
- Negative & Edge Cases (10 tests)
- End-to-End Flow (2 tests)

**Total: 32 test cases**

## Getting Started

```bash
# Install dependencies
npm install

# Run tests
npx playwright test

# Run specific test file
npx playwright test tests/automated-tests/search_functionality.spec.ts
```

## Notes

- Amazon.in implements bot detection which may cause 503 errors
- Tests may require stealth configuration or manual testing approach
- See `specs/execution-results.md` for detailed execution logs
