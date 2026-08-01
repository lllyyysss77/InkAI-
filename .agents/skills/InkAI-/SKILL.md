```markdown
# InkAI- Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill introduces the core development patterns and workflows used in the InkAI- Python codebase. It covers file organization, code style, commit conventions, documentation workflows, and testing patterns. By following these guidelines, contributors can ensure consistency, maintainability, and clarity throughout the project.

## Coding Conventions

### File Naming
- Use **snake_case** for all file and module names.
  - **Example:**  
    `text_processor.py`, `data_loader.py`

### Import Style
- Use **relative imports** within the package.
  - **Example:**
    ```python
    from .utils import load_config
    from .models.text_generator import TextGenerator
    ```

### Export Style
- Use **named exports** (explicitly define what is exported from a module).
  - **Example:**
    ```python
    __all__ = ['TextGenerator', 'load_config']
    ```

### Commit Messages
- Follow **conventional commit** format.
  - Prefixes: `feat`, `docs`
  - **Examples:**
    - `feat: add text generation module`
    - `docs: update usage section in README`

## Workflows

### Update README and README_CN
**Trigger:** When documentation needs to be updated to reflect new features, architecture changes, or to add feedback channels.  
**Command:** `/update-readmes`

1. Edit `README.md` to add or update project information, architecture diagrams, issue fix cases, or feedback channels.
2. Edit `README_CN.md` to mirror the changes in Chinese.
3. Optionally update related documentation or requirements if needed.
4. Commit both `README.md` and `README_CN.md` together with a descriptive commit message.
   - **Example commit:**  
     `docs: update architecture diagram in README and README_CN`

## Testing Patterns

- **Framework:** Not explicitly specified; may use standard Python testing tools.
- **Test File Pattern:** Test files are named with the pattern `*.test.*`
  - **Example:**  
    `text_generator.test.py`
- **Test Example:**
  ```python
  def test_text_generation():
      generator = TextGenerator()
      result = generator.generate("Hello")
      assert isinstance(result, str)
  ```

## Commands

| Command           | Purpose                                                            |
|-------------------|--------------------------------------------------------------------|
| /update-readmes   | Synchronize and update both English and Chinese README files.       |
```
