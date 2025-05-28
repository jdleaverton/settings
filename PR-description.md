# PR Description Generation Guide for AI Assistant

I am requesting a PR Description. The following is style guides on how you should return the description to me.

## I. Overall Structure & Tone:

1.  **Conciseness & Information Density**: Every sentence should convey meaningful information. Avoid filler, verbose explanations, or details that a senior developer would find obvious.
2.  **Target Audience**: Assume senior developers who are familiar with the codebase and require a quick understanding of significant changes.

## II. Content - "Key Changes" Section:

This section will form the core of the PR description.

1.  **Logical Grouping**: Group related changes under descriptive sub-headings. These often correspond to services, modules, or significant features affected.
2.  **Detailing Changes**:
    *   For each group, list the most important modifications.
    *   Specify *what* changed and *how* it changed. For instance, instead of "improved X", state "X now does Y by implementing Z".
    *   Mention new methods, parameters, or significant modifications to existing ones.
    *   Highlight key configuration changes or updates to initialization logic.
3.  **Testing Context**:
    *   Briefly mention significant additions or updates to tests that validate the core changes. E.g., "Added integration tests for..." or "Updated unit tests to mock X and verify Y."
    *   Do not list every minor test modification.
4.  **Dependency Updates**:
    *   Create a "Dependency Updates" sub-section if there are changes to project dependencies.
    *   List major version bumps for existing dependencies (e.g., `package-name: ^1.0.0 -> ^2.0.0`).
    *   List newly added or removed dependencies.
    *   **CRITICAL**: Do NOT mention updates to lock files (e.g., `poetry.lock`, `package-lock.json`).

## III. Formatting:

1.  Use markdown for all formatting.
2.  Employ bullet points for lists of changes within sub-sections to enhance readability.
3.  Use backticks (`) for inline code elements like function names, variable names, file names, and versions.

## IV. Example Snippet (Illustrative - Adapt to Actual Changes):

```markdown
## Key Changes

### Service X: New Feature Y Integration
-   `NewClassOrFunction` introduced to handle Y processing.
-   `ExistingFunction` in `module_a.py` now accepts `new_parameter: type` to support Y.
-   GraphQL mutation `performY` added with fields `field1, field2`.
-   Configuration `ENABLE_FEATURE_Y` in `config.toml` now defaults to `true`.
-   Added integration tests in `tests/integration/test_feature_y.py`.

### Core Library Z: Performance Enhancement
-   Refactored `CriticalComponent` to use `NewAlgorithm`, reducing latency by X%.
-   WebSocket client schema now directly initialized from `SchemaManager` to prevent redundant fetches.
-   Updated `test_critical_component.py` to include benchmarks for `NewAlgorithm`.

### Dependency Updates
-   Project version: `1.4.0` -> `1.4.1`.
-   `some-library`: `^2.3.0` -> `^2.5.1`.
-   Added `new-dependency: ^1.0.0`.
```

By following this guide, you should generate PR descriptions that are aligned with my preferences.
