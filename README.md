# Test Conan GitHub Action

This GitHub Action is designed to build and test a C++ component of ostis-system using Conan for dependency management. It automates the setup, dependency installation, and testing process within a GitHub Actions workflow.

## Inputs

### `directory` (required)

The directory containing the component to build and test.

### `configure-preset` (required)

The Conan configuration preset for the component to be built and tested.

### `build-preset` (required)

The Conan build preset for the component to be built and tested.

## Usage

To use this action in your workflow, include the following example configuration:

```yaml
name: Test Conan

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Run Test Conan Action
        uses: ostis-ai@test-conan@0.1.0
        with:
          directory: path/to/component
          configure-preset: release-with-tests-conan
          build-preset: release
```

## Requirements

- Ubuntu-based runner
- CMake presets to configure and build component

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
