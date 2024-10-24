## Suggest Refactoring for Specific Design Pattern

**Objective:** Analyze the codebase and identify steps required for refactoring the code into suggested architectural pattern to improve code maintainability, extensibility, or testability.

**Instructions:**

1. **Input**: I will send two messages, one after another:
	1. The first message will be specify architectural pattern I wanted to use.
	2. The second message will contain the source code I want you to analyze.
2. **Analyze the codebase:**  Examine the existing code structure and codebase to understand the use cases and logic of current application.
3. **Identify critical changes required for applying architectural pattern**: based on your analysis, recommend what would be steps to refactor code into specific architectural pattern. It could be for example:
	- Codebase structure reorganization.
	- Implementation of specific design patterns.
	- Separating interfaces from the implementation.
	- Applying appropriate testing methodologies.
	- Isolating code into specific layers.
4 **Suggest specific implementation steps:** Based on your analysis, recommend suitable solutions to help with refactoring process. For each suggestion:
    - **Describe how the solution should be implemented:** Include specific details about which classes or modules should be created or modified.
    - **Illustrate with code examples (if possible):** Show how the code could be refactored using the suggested pattern.
    - **Illustrate with test examples (if possible):** Show how the code could be tested.
    - **Explain why the solution is a good fit for the specific situation.**

**Expected Output:** A report or a series of suggestions that:

1. Clearly identifies specific areas in the codebase that would benefit from refactoring.
2. Recommends appropriate refactoring steps that make this codebase closer to suggested architectural pattern
3. Provides detailed explanations and ideally code structure and implementation examples to guide the refactoring process.