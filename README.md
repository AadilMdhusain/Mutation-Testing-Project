<H1> Booking System - A Software Testing Project</H1>

We have implemented mutation testing using PIT (Pitest) to evaluate and strengthen the test quality of our Restaurant Booking System backend.
The aim of this implementation is to go beyond traditional code coverage and ensure that our unit tests are capable of detecting real faults in the booking logic.

While normal coverage metrics only indicate how much of the code is executed during tests, mutation testing measures how effective those tests truly are. PIT achieves this by automatically injecting small changes—called mutations—into the source code and observing whether the existing test suite detects these changes.
If a mutation goes undetected, it highlights gaps in test assertions, missing edge cases, or insufficiently validated business logic.

Beyond validating individual units, our objective was to extend mutation testing to cover the overall API and business logic of the Booking System. Instead of restricting PIT to isolated methods, we applied mutation testing across service-layer workflows to observe how well the system’s end-to-end logic is protected by our tests. This includes validating booking rules, restaurant capacity checks, date and time constraints, customer–restaurant mappings, and error-handling scenarios. By doing so, mutation testing goes beyond simple unit validation and becomes a tool for verifying the resilience and correctness of the entire business flow, ensuring that both API behavior and core business logic remain robust even under unexpected or faulty conditions.

The entire code base of the project is available [here](https://github.com/AadilMdhusain/Mutation-Testing-Project).

<H5>Testing Tools:</H5>
JUnit 5
Used for writing comprehensive Unit and Integration Tests across all backend services. JUnit 5 (brought in through the Spring Boot 3.2.5 starter) enables parameterized testing, structured test suites, and modern assertion APIs—ensuring maintainable, expressive, and well-organized test cases.

PIT Mutation Testing (Pitest 1.17.1)
Integrated via the Pitest Maven Plugin to measure the effectiveness of the test suite rather than just execution coverage. PIT automatically introduces code mutations, evaluates whether the tests can detect them, and generates detailed HTML reports. This provides deeper insights into untested logic paths, weak assertions, and potential blind spots in the booking service.

<H5>Schema of the Project</H5>
The Schema of the project goes as follows:

<img src="Schema.png" alt="Schema" width="600" height="auto">

<H5>Types of Mutators Used:</H5>

The following PIT mutation operators were enabled to thoroughly test conditionals, method behavior, return values, arithmetic operations, and constants within the Booking System:

🔹 Conditional Mutators

CONDITIONALS_BOUNDARY

NEGATE_CONDITIONALS

REMOVE_CONDITIONALS_EQUAL_ELSE

REMOVE_CONDITIONALS_EQUAL_IF

REMOVE_CONDITIONALS_ORDER_ELSE

REMOVE_CONDITIONALS_ORDER_IF

🔹 Method Call Mutators

VOID_METHOD_CALLS

NON_VOID_METHOD_CALLS

CONSTRUCTOR_CALLS

🔹 Return Value Mutators

EMPTY_RETURNS

FALSE_RETURNS

TRUE_RETURNS

NULL_RETURNS

PRIMITIVE_RETURNS

🔹 Arithmetic & Number Mutators

INCREMENTS

REMOVE_INCREMENTS

INVERT_NEGS

MATH

🔹 Constants Mutator

INLINE_CONSTS

<H3>The Results of the Mutation Testing are as follows:</H3>

Overall Test Report:

<img src="OverallTestReport.png" alt="Overall Test Report" width="600" height="auto">

Unit Testing:

<img src="UnitTestingReport.png" alt="Unit Testing" width="600" height="auto">

Integration Testing:

<img src="IntegrationTestingReport.png" alt="Integration Testing" width="600" height="auto">
