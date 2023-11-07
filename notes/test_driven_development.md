# Test Driven Development

# Table of Contents
1. [Benefits of Test Driven Development](#tdd_benefits)
2. [Tools for TDD](#tdd_tools)
3. [Running Tests with Nose](#runnnig_tests_with_nose)
4. [Anatomy of a Test Case](#test_case_anatomy)
5. [Writing Test Assertions](#test_assertions)
6. [Test Fixtures](#test_fixtures)
7. [Creating Initial State Using Test Fixtures](#create_initial_state_with_test_fixtures)

---

<a id="tdd_benefits"></a>
# Benefits of Test Driven Development
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Test-Driven Development (TDD) and Its Benefits for DevOps

## What is TDD?
- **Definition:** TDD is a software development approach where unit test cases are written to drive the design of the code.

## Red/Green/Refactor Workflow
- **Red:** Write a failing test case for the desired code functionality.
- **Green:** Write just enough code to make the test case pass.
- **Refactor:** Improve and clean up the code without changing its behavior.

## Benefits of TDD for DevOps
- **Time Efficiency:** Quick test feedback helps developers fix breaks as features are written or modified.
- **Coding Confidence:** Test cases provide a safety net for refactoring and adding new features.
- **Quality Assurance:** Test cases verify that code changes don't introduce new bugs.
- **CI/CD Integration:** Automated testing is crucial for Continuous Integration and Continuous Delivery pipelines.

<!-- /MarkdownTOC -->
</details>

---

<a id="tdd_tools"></a>
# Tools for TDD
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Popular Testing Tools for TDD

## Popular Testing Frameworks for TDD
- **xUnit Series:**
  - **JUnit:** Java
  - **PyUnit/unittest:** Python
  - **NUnit:** .NET
  - **Embunit:** C/C++
- **Other Frameworks:**
  - **Jasmine:** JavaScript
  - **Mocha:** Node.js
  - **SimpleTest:** PHP

## Python Testing Tools
- **PyUnit (unittest):**
  - Built into Python.
  - Familiar to most Python developers.
- **Pytest:**
  - Supports multiple levels of setups and teardowns.
  - Not preferred if PyUnit suffices and to avoid extra dependencies.
- **Doctest:**
  - Allows writing tests in docstrings.
  - Limited and not scalable for complex code.
- **RSpec (for Ruby):**
  - Syntax supported by Python.
  - Good choice for those familiar with Ruby's RSpec.

## Additional Python Testing Tools
- **Nose:**
  - Test runner that enhances output with color and formatting.
  - Can integrate with coverage tools.
- **Coverage Tool:**
  - Measures code coverage percentage.
  - Generates reports on unexecuted code for targeted test case writing.

## Conclusion
- **The xUnit series is highly popular across different programming languages.**
- **PyUnit and Pytest are the most popular for Python testing, with Nose and coverage tools providing additional testing support.**

<!-- /MarkdownTOC -->
</details>

---

<a id="runnnig_tests_with_nose"></a>
# Running Tests with Nose
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Running Unit Tests with `unittest` and `Nose`

## Running Tests with `unittest`
- Invoke Python with the `unittest` module to discover and run tests.
- Tests are indicated by dots for success or "F" for failure.
- The report shows the total number of tests run and the time taken.

## Running Tests with `Nose`
- `Nose` is used for "sniffing" out bugs with more informative output.
- Use the `nosetests` command with additional parameters for color output.
- `Pinocchio` plugin adds color to the test output.
- Verbose output with descriptions from test case docstrings.
- Integrates with coverage tools to report code coverage statistics.
- Lists specific lines of code that are missing test cases.

## Comparison of Reports
- `unittest` provides a basic report with minimal information.
- `Nose` offers detailed, color-coded reports with descriptive test names.
- It also reports on code coverage and helps identify untested code lines.

---

# Video Summary: Running Tests with `unittest` and `Nose`

## Using `unittest`
- Run tests from the command line with Python's `unittest` module.
- Results are indicated by dots for each test, with "E" for errors.
- Verbose mode (`-v`) can be enabled for more output.

## Using `Nose`
- Install `Nose` to run tests with `nosetests` command.
- By default, `Nose` behaves like `unittest`.
- Verbose output with `nosetests -v` shows docstring descriptions.

## Enhancing `Nose` with Pinocchio Plugin
- Install `Pinocchio` for specification-style output (`--with-spec`) and colorized test results (`--spec-color`).
- Test failures will be highlighted in red.

## Integrating Coverage Tool with `Nose`
- Install `coverage` to report on code coverage.
- Use `--with-coverage` for coverage reports and `--cover-erase` to avoid cumulative misleading coverage data.
- Use `coverage report -m` to show missing lines not executed by tests.

## Automating Configuration with `setup.cfg`
- Create a `setup.cfg` file to specify `Nose` and coverage options without command-line flags.
- Include verbosity, specification, color, and coverage configurations.
- Running `nosetests` will now use these configurations, providing detailed and colorized output, as well as coverage reports with missing lines.

<!-- /MarkdownTOC -->
</details>

---

<a id="test_case_anatomy"></a>
# Anatomy of a Test Case
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Test Fixtures, Frameworks, and Writing Test Cases

## Role of Test Fixtures in Testing
- **Definition:** Test fixtures set up an initial state before tests run and clean up after they are finished.
- **Implementation:** Use `setUp()` to initialize and `tearDown()` to reset or clean up after a test case.
- **Example:** In stack tests, `setUp()` creates a new stack instance and `tearDown()` sets it to `None`.

## How Test Frameworks Help Build Assertions
- **Purpose:** Test frameworks, like Python's `unittest`, provide a set of methods to assert conditions in code.
- **Assertions:** These methods allow developers to check for expected outcomes, such as `assertEqual()` or `assertTrue()`.
- **Inheritance:** Test case classes inherit from `TestCase` to use these assertion methods.

## Constructing Test Cases
- **Structure:** Define a class that is a subclass of `TestCase` and includes test methods starting with `test`.
- **Example Test Cases:** 
  - `test_push()` to verify pushing an item onto the stack.
  - `test_pop()` to confirm popping the top item off the stack and ensuring the stack is empty afterward.

## Summary of Learning Points
- Test fixtures prepare and clean up the test environment for each test case.
- Testing frameworks provide assertion tools to confirm code behavior.
- Test cases are methods within a subclass of `TestCase` that check the functionality of the code under test.

<!-- /MarkdownTOC -->
</details>

---

<a id="test_assertions"></a>
# Writing Test Assertions
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Video Summary: Assertions and Path Testing in PyUnit

## Purpose of Assertions
- **Function:** Assertions evaluate to True or False to determine if a test passes or fails.
- **Behavior:** They raise an exception if they evaluate to False, marking the test as failed.

## Common PyUnit Assertions
- **Basic Assertion:** `assert()` function call.
- **PyUnit Assertions:** `TestCase` provides additional assertions for cleaner syntax.
  - `assertEqual(a, b)`: Asserts that `a` is equal to `b`.
  - `assertNotEqual(a, b)`: Asserts that `a` is not equal to `b`.
  - `assertIn(a, b)`, `assertNotIn(a, b)`: Check for membership in a collection.
  - `assertTrue()`, `assertFalse()`: Check if a value is True or False.
  - `assertIsInstance(a, TYPE)`: Asserts `a` is of `TYPE`.
  - `assertRaises()`: Checks if a specific exception is raised.

## Role of Happy Paths and Sad Paths in Testing
- **Happy Paths:** Test scenarios where everything goes as planned, confirming expected positive outcomes.
- **Sad Paths:** Scenarios where something is expected to go wrong, verifying that the function handles exceptions properly.
  - Use `assertRaises()` to check for proper handling of invalid inputs or conditions.

---

# Video Summary: Assertions and Path Testing in PyUnit

## Purpose of Assertions
- **Function:** Assertions evaluate to True or False to determine if a test passes or fails.
- **Behavior:** They raise an exception if they evaluate to False, marking the test as failed.

## Common PyUnit Assertions
- **Basic Assertion:** `assert()` function call.
- **PyUnit Assertions:** `TestCase` provides additional assertions for cleaner syntax.
  - `assertEqual(a, b)`: Asserts that `a` is equal to `b`.
  - `assertNotEqual(a, b)`: Asserts that `a` is not equal to `b`.
  - `assertIn(a, b)`, `assertNotIn(a, b)`: Check for membership in a collection.
  - `assertTrue()`, `assertFalse()`: Check if a value is True or False.
  - `assertIsInstance(a, TYPE)`: Asserts `a` is of `TYPE`.
  - `assertRaises()`: Checks if a specific exception is raised.

## Role of Happy Paths and Sad Paths in Testing
- **Happy Paths:** Test scenarios where everything goes as planned, confirming expected positive outcomes.
- **Sad Paths:** Scenarios where something is expected to go wrong, verifying that the function handles exceptions properly.
  - Use `assertRaises()` to check for proper handling of invalid inputs or conditions.

<!-- /MarkdownTOC -->
</details>

---

<a id="test_fixtures"></a>
# Test Fixtures
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Video Summary: The Purpose and Use of Test Fixtures in Testing

## Purpose of Using Test Fixtures
- **Initial State:** Test fixtures set up a known state before running tests.
- **Isolation:** They ensure tests run in isolation and system is reset after each test.
- **Repeatability:** Consistent starting state guarantees repeatable results.

## Situations Where Test Fixtures Are Useful
- **Data Preparation:** For setting up databases or loading specific data sets.
- **Environment Configuration:** Creating necessary files, directories, or mock objects.
- **State Consistency:** Ensuring tests start with the same environment each time.

## Using Test Fixtures for Initial State
- **PyUnit Fixtures:**
  - `setUpModule()`: Runs once before the entire module.
  - `tearDownModule()`: Runs once after all tests in the module.
  - `setUpClass()`: Runs once before all tests in a class.
  - `tearDownClass()`: Runs once after all tests in a class.
  - `setUp()`: Runs before each individual test.
  - `tearDown()`: Runs after each individual test.

## Example of Test Fixtures in PyUnit
- **Database Connection:** `setUpClass()` to connect and `tearDownClass()` to disconnect.
- **Table Management:** `setUp()` to recreate tables and `tearDown()` to clear them after each test.
- **Data Loading:**
  - Global or class-level dictionaries to hold test data.
  - Load data from JSON or other files into the test environment using `setUpClass()`.

## Test Fixtures for Account Testing
- **Folder Structure:** A `fixtures` folder contains data files like `account_data.json`.
- **Data Usage:** A global dictionary holds the data, loaded in `setUpClass()`, and used to create accounts in tests.

<!-- /MarkdownTOC -->
</details>

---

<a id="create_initial_state_with_test_fixtures"></a>
# Creating Initial State Using Test Fixtures
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---
