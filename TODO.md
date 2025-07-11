# TODO: MCP Client Test & Type Annotation Roadmap

## Features to Implement

1. **Type Annotations**
   - Add and refine type annotations for all functions, methods, and class attributes in `client.py`.
   - Use MCP library documentation to ensure correct types.
   - Integrate static type checking (e.g., mypy) into the workflow.

2. **Test Suite Structure**
   - Create a `tests/` directory for all test code.
   - Use `pytest` as the main testing framework.
   - Add development dependencies for testing and type checking.

3. **Test Coverage Goals**
   - Unit tests for all public methods in the client class.
   - Integration tests for client logic (mocking MCP server responses).
   - Edge case tests for error handling and invalid input.
   - Tests for CLI argument parsing and main entry point behavior.

4. **Mocking External Dependencies**
   - Mock MCP server interactions and Google API calls in tests.
   - Ensure tests do not require a real MCP server or API key.

5. **Automation**
   - Add scripts or CI configuration to run tests and type checks automatically.
   - Monitor test coverage with tools like `pytest-cov`.

---

*Implementation will begin after reviewing the MCP library documentation for accurate type hints.*