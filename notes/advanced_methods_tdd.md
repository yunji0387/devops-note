# Advanced Methods for Test Driven Development

# Table of Contents
1. [Test Coverage](#test_coverage)
2. [Running Test Cases with Coverage](#running_test_cases_with_coverage)
3. [Factories and Fakes](#factories_and_fakes)
4. [Mocking](#mocking)
5. [Mocking with Patch](#mocking_with_patch)
6. [Mocking with Mock Objects](#mocking_with_mock_objects)
7. [Practicing Test Driven Development](#practicing_tdd)

---

<a id="test_coverage"></a>
# Test Coverage
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# The Importance of Test Coverage

## Understanding Test Coverage
- **Definition:** Test coverage measures the percentage of executable code lines that tests run.
- **Purpose:** High test coverage provides confidence in code functionality.

## Utilizing Test Coverage Reports
- **Functionality:** Coverage reports show which lines of code were or were not executed by tests.
- **Actionable Insights:** They highlight where to write additional tests for untested code.

## Enhancing Test Coverage
- **Identifying Untested Code:** Use the `-m` option with coverage tools to reveal untested lines.
- **Developing Test Cases:** Create tests to execute untested lines, aiming to increase the coverage percentage.

## Importance of Testing Both Happy and Sad Paths
- **Happy Paths:** Test cases where the expected, correct outcomes occur.
- **Sad Paths:** Test cases that handle errors or unexpected inputs.
- **Comprehensive Testing:** Coverage must include both paths for thorough validation.

## Continual Testing Beyond 100% Coverage
- **Beyond the Percentage:** 100% test coverage doesn't guarantee bug-free code.
- **Testing with Bad Data:** Continue to challenge code with unexpected inputs and edge cases.

<!-- /MarkdownTOC -->
</details>

---

<a id="running_test_cases_with_coverage"></a>
# Running Test Cases with Coverage
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Video Summary: Running Test Cases with Coverage

## Introduction to Test Coverage
- Test coverage indicates how much of the code is executed by tests.
- It is measured as the percentage of total executable lines that tests run.
- High coverage offers more confidence that the code works correctly.

## Using Coverage Reports
- Coverage reports identify both tested and untested lines of code.
- They guide developers on where to focus when writing additional tests.

## Steps to Increase Test Coverage
1. **Run Coverage Tool:** Begin with running the coverage tool to get a baseline report.
2. **Identify Missing Lines:** Use `-m` option to highlight lines without test coverage.
3. **Review Code:** Examine the untested lines to understand their function within the code.
4. **Write Test Cases:** Develop tests specifically to cover these lines, both happy and sad paths.

## Example Workflow
- Start by creating an account and asserting its creation.
- Update the account and assert changes are reflected.
- Test deletion of an account and assert it no longer exists.
- For each function (e.g., string representation, dictionary conversion, update, delete), write tests that ensure coverage.

## Importance of Testing All Code Paths
- **Happy Paths:** Standard operations where functions perform as expected.
- **Sad Paths:** Error handling and edge cases that might not be covered by initial tests.
- **Comprehensive Testing:** Achieve 100% coverage by testing all paths, ensuring robustness.

## Continuous Testing Beyond 100% Coverage
- Even at 100% coverage, continue testing with varied data and scenarios.
- Full coverage does not mean the absence of bugs, so keep challenging the code.

<!-- /MarkdownTOC -->
</details>

---

<a id="factories_and_fakes"></a>
# Factories and Fakes
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Factories and Fakes for Testing

## Generating Fake Data for Tests
- **Factories** help in creating realistic test data.
- **Fakes** are simulated versions of classes with realistic data for testing.
- **FactoryBoy** is a Python tool used to generate fake data, similar to Ruby's FactoryGirl.

## Creating Data Models for Testing
- **SQLAlchemy** ORM is used to define data models.
- **Model Definition:** Includes attributes like id, name, email, phone, disabled status, and date joined.
- **Fake Data Requirements:** The fields in the Account data model serve as a blueprint for the fake data.

## Using FactoryBoy for Fake Data
- Import FactoryBoy and define a factory class, such as `AccountFactory`.
- Use `Faker` for attributes that have a corresponding provider (e.g., name, email, phone number).
- Use `FuzzyChoice` for attributes without a direct provider, such as Booleans.
- `LazyFunction` and `datetime` can generate timestamps when creating fake data instances.

## Implementing Factories in Unit Testing
- Instantiate `AccountFactory` and use it like a real model instance.
- Create, update, and assert operations on `AccountFactory` as if it were the real `Account` class.
- Factories allow for testing with a variety of realistic data scenarios.

## Providers Supported by Faker
- Faker offers a range of standard providers for generating data like addresses, companies, jobs, etc.
- Custom and community providers expand the possibilities of fake data generation.

## Fuzzy Attributes for Diverse Data Types
- FactoryBoy's `FuzzyChoice` and other fuzzy attributes provide random data for various types.

---

# Video Summary: Using Factories and Fakes in Testing

## Introduction to Factories and Fakes
- Factories help generate dynamic test data, replacing the need for fixed test fixtures.
- Fakes are simulated versions of classes that can be used in tests.
- FactoryBoy is used in Python to create factories similar to Ruby's FactoryGirl.

## Setting Up the Factory
- Start by creating a base factory class with FactoryBoy.
- Define attributes in the factory corresponding to the model class attributes.
- Use Faker within FactoryBoy to generate realistic attribute values.

## Defining Factory Attributes
- **ID:** Use FactoryBoy's `Sequence` to generate a sequence of numbers.
- **Name, Email, Phone Number:** Use `Faker` to create fake names, emails, and phone numbers.
- **Disabled (Boolean):** Use `FuzzyChoice` to randomly select between `True` or `False`.
- **Date Joined:** Use `FuzzyDate` to generate random dates from a specified start date.

## Implementing the Factory in Tests
- Import `AccountFactory` from the factory module.
- Replace instances where fixed data from JSON fixtures is used with `AccountFactory`.
- Create, update, and assert operations on `AccountFactory` instances just like with real models.

## Running Tests with the Factory
- Eliminate the need for a pre-existing JSON fixture by directly using the `AccountFactory`.
- Update test cases to instantiate `AccountFactory` and perform test assertions.
- Use `nose tests` to run tests and validate the successful integration of the factory.

## Benefits of Using Factories and Fakes
- Generate large volumes of realistic test data on the fly.
- Mimic real-world data models without the overhead of setting up and maintaining extensive test fixtures.
- Enhance testing by ensuring no dependency on the order of tests and allowing for randomization.

## Conclusion
- Factories and fakes provide a powerful way to generate dynamic test data.
- They allow for more flexible and comprehensive testing scenarios.
- FactoryBoy and Faker offer extensive capabilities to customize test data generation.

<!-- /MarkdownTOC -->
</details>

---

<a id="mocking"></a>
# Mocking
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Understanding Mocking in Testing

## What is Mocking?
- Mocking involves creating objects that simulate the behavior of real objects.

## Why Mock?
- Useful when your code depends on external systems (e.g., APIs, databases).
- Avoids issues like overloading external services or handling service downtime during tests.
- Isolates the test to focus solely on your code.

## Advantages of Mocking
- Allows testing of your code’s interaction with the external system.
- Gives control over the data returned from the mocked system for testing various scenarios.
- Enables testing of error handling by simulating failures and unexpected behavior.

## When to Use Mocking
- To isolate tests from remote components or external systems.
- When a part of the application isn't available during testing.

## Methods of Mocking
- **Patching:** Changes the behavior of function calls, including those from third-party libraries.
- **Mock Objects:** Stand in for entire objects, not just function calls, changing the object’s behavior.
  - Python's PyUnit includes Mock and MagicMock objects for this purpose.

## Key Points
- Mock objects mimic real objects' behaviors for testing purposes.
- Mocking is essential for isolating tests from dependencies on external systems.
- Developers can use patches to simulate different conditions and change function behaviors.
- Mock objects can replace entire objects to verify interactions and behaviors.

<!-- /MarkdownTOC -->
</details>

---

<a id="mocking_with_patch"></a>
# Mocking with Patch
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Understanding Patching in Python's Mock Library

## What is Patching?
- Patching is a mocking technique used to change the behavior of a function call.
- It is particularly useful for simulating interactions with external systems or for creating error conditions during testing.

## When to Use Patching
- When the function calls an external system not under your control.
- When simulating error conditions without causing actual errors.

## Python Mock Library Patching Techniques
- **Patching a function’s return value:** 
  - Allows you to control the return value of a function.
  - Useful for testing error handlers by returning error condition codes.
  - Controls the data returned from a function call by returning any data structure or object the program expects.

- **Replacing a function with another function (Side Effect):**
  - Enables you to replace the actual function with a custom one to simulate different behaviors.
  - Useful when you need to simulate more complex behaviors or a series of function calls or effects.

## Examples of Patching
- **Patching a function's return value:**
  - Using `with` to patch `imdb_info` function to return a status code of 200.
  - Confirming that the actual function code is bypassed.

- **Patching a third-party library function:**
  - Patching `requests.get()` to return a specified value without making a real API call.

- **Using a Side Effect:**
  - Defining custom functions `bye()` and `hello()` and using patching to replace the call to `hello()` with `bye()` during testing.

## Key Points
- Patching allows for precise control over the behavior of functions during testing.
- By using patching, developers can simulate both successful and error conditions.
- Patching can be applied to both functions you've written and third-party library functions.
- Python's `unittest.mock` library provides both `return_value` patching and `side_effect` patching for comprehensive testing scenarios.

<!-- /MarkdownTOC -->
</details>

---

<a id="mocking_with_mock_objects"></a>
# Mocking with Mock Objects
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="practicing_tdd"></a>
# Practicing Test Driven Development
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---
