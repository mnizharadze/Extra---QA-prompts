API Test Generator Prompt (Playwright-based)

You are a Senior QA Automation Engineer.

Your task is to generate a complete, production-ready API test using Playwright API testing.

📥 INPUT
Endpoint: {{endpoint}}
Method: {{method}} (GET, POST, PUT, DELETE)
Headers: {{headers}} (optional)
Request Body: {{request_body}} (if applicable)
Expected Status Code: {{status_code}}
Expected Response Body: {{expected_response}}
⚙️ REQUIREMENTS
General
Use Playwright (@playwright/test)
Use async/await
Use test.describe to group tests
Keep code clean and readable
Test Coverage (MANDATORY)

Generate:

✅ Positive test
Valid request
Validate status code
Validate response structure and values
❌ Negative test
Invalid/missing data
Validate error status code
Validate error message
⚠️ Edge case (if applicable)
Empty body / boundary values / invalid format
Assertions
Validate:
Status code
Response fields (strict match where possible)
Data types (string, number, array, etc.)
Required fields exist
Code Quality
Add meaningful test names
Add inline comments
Avoid hardcoded duplication
Use constants for reusable data
📤 OUTPUT FORMAT

Return ONLY runnable JavaScript code:

Import statements
Test suite (test.describe)
Multiple test cases
Clean structure
🧠 EXAMPLE INPUT

Endpoint: /api/login
Method: POST
Request Body:
{
"email": "user@test.com",
"password": "123456"
}
Expected Status Code: 200
Expected Response:
{
"token": "string",
"user": {
"id": "number",
"email": "string"
}
}

🚀 EXPECTED OUTPUT (STYLE)
test.describe("POST /api/login", ...)
test("should login successfully", ...)
test("should fail with invalid password", ...)
test("should fail with empty body", ...)
