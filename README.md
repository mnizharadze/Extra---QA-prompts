# 🧠 AI-Powered QA Automation Framework

This project demonstrates a **modern QA Automation framework enhanced with AI-driven prompt engineering and self-healing capabilities**.

It combines:

* UI Test Automation (Playwright + POM)
* API Test Automation
* Reusable AI Prompt Library
* Self-maintaining test mechanism

---

# 📁 Project Structure

```
project/
│
├── qa-library/                # Reusable AI prompts
│   ├── ui-test-generator.md
│   ├── api-test-generator.md
│   └── test-case-generator.md
│
├── pages/                    # Page Object Models
├── tests/                    # UI test specs
├── api/                      # API test specs
├── utils/                    # Helper functions
│
├── snapshots/                # HTML snapshots (for self-healing)
├── .github/workflows/        # CI/CD configuration
│
├── package.json
└── README.md
```

---

# 🚀 Getting Started

## 1. Install dependencies

```bash
npm install
```

---

## 2. Install Playwright

```bash
npx playwright install
```

---

## 3. Run tests

### ▶️ Run all tests

```bash
npx playwright test
```

### ▶️ Run UI tests only

```bash
npx playwright test tests/
```

### ▶️ Run API tests only

```bash
npx playwright test api/
```

---

# 🧠 AI Prompt Library

The `qa-library/` folder contains **reusable prompts** used to generate:

* 🧪 API tests
* 🖥️ UI automation scripts (POM-based)
* 🧾 Test cases

---

## ✨ How it works

1. Prompts are written in structured format
2. They are used inside AI tools (e.g. Cursor)
3. AI generates:

   * Test scripts
   * Page Objects
   * Test cases

---

## 🧪 Example Usage

In Cursor:

```
Use api-test-generator.md to generate test for:
POST /api/login
```

👉 Output: fully working Playwright API test

---

# 🔄 Self-Healing Test Mechanism

This project includes an **AI-based test update system**.
Prompt library is designed to support self-healing by:
- Generating resilient locators
- Adapting tests to UI changes
- Enabling easy regeneration of broken selectors
---

## ⚙️ როგორ მუშაობს

### 1. HTML Snapshot Capture

Tests store DOM structure:

```js
const html = await page.content();
```

---

### 2. Change Detection

Old vs new HTML is compared to detect UI changes.

---

### 3. Locator Failure

If a locator breaks:

```js
page.locator('#login-btn') // fails
```

---

### 4. AI Locator Regeneration

AI analyzes:

* Old HTML
* New HTML
* Old locator

👉 Generates new locator:

```js
page.locator('button:has-text("Login")')
```

---

### 5. Auto Update

Tests are updated dynamically or via fallback locators.

---

## 🎯 Goal

✔ Reduce maintenance
✔ Automatically adapt to UI changes
✔ Create resilient test suite

---

# 🌐 Real Project Testing

This framework can be applied to real systems such as:

* izibox
* optimo
* biletebi
* extra

---

# 🔧 CI/CD Integration

GitHub Actions is used for automated test execution.

### Example workflow:

```yaml
name: Run Tests

on: [push]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3
      - run: npm install
      - run: npx playwright install
      - run: npx playwright test
```

---

# 📊 Evaluation Criteria Coverage

This project satisfies:

* ✅ Test Case Quality
* ✅ POM Implementation
* ✅ API Coverage
* ✅ AI Prompt Quality
* ✅ Self-Healing Mechanism
* ✅ GitHub Structure

---

# 🧠 AI Usage Explanation

Prompts were:

1. Initially generated with AI assistance
2. Refined manually for:

   * Better structure
   * Reusability
   * Accuracy

AI is used for:

* Test generation
* Locator regeneration
* Reducing manual effort

---

# 🧨 Bonus Features (Optional)

* Parallel execution
* Visual testing (snapshots)
* Allure reporting
* Test data generation (faker)

---

# 🎥 Demo

The project demo includes:

* Running UI & API tests
* AI-generated tests
* Self-healing mechanism in action

---

# 📌 Conclusion

This project demonstrates how **AI can significantly enhance QA Automation** by:

* Automating test creation
* Reducing maintenance
* Enabling self-healing systems

---

# 👨‍💻 Author

QA Automation Student Project
