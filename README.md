# Snake Game Tests

Snake Game Tests is a simple comparison project for testing AI coding models and coding environments using the same programming challenge.

The aim is straightforward:

**Each test run must create a complete, playable Snake game contained entirely within a single HTML file named `classic_snake.html`.**

The same model may be tested multiple times under different environments, tools, configurations, or inference conditions.

## Standard Test Prompt

> Create a complete, playable Classic Snake Game in a single HTML file named `classic_snake.html`.
>
> Use HTML, CSS and JavaScript only.
>
> Everything required to run the game must be contained within that one HTML file.
>
> The game must work when `classic_snake.html` is opened directly in a web browser.
>
> Do not use external libraries, frameworks, images, assets or additional files.

## What Is Being Compared

The project is designed to compare both:

* **Model capability**
* **The effect of the surrounding coding environment**

A single model may therefore appear in several tests, for example:

* Direct model output
* Hermes
* OpenCode
* VS Code agent
* Different tool configurations
* Different context or token settings
* Local versus hosted inference

This makes it possible to see whether differences in results come from the model itself, the environment around it, or both.

## Test Structure

Each test run should have its own folder.

```text
tests/
└── model-name/
    └── environment/
        └── condition/
            ├── classic_snake.html
            └── TEST.md
```

Example:

```text
tests/
└── qwen3.8-27b/
    ├── hermes/
    │   ├── default/
    │   │   ├── classic_snake.html
    │   │   └── TEST.md
    │   └── tools-disabled/
    │       ├── classic_snake.html
    │       └── TEST.md
    │
    └── opencode/
        └── default/
            ├── classic_snake.html
            └── TEST.md
```

## Test Metadata

Every submission should include a `TEST.md` file beside the generated game.

At minimum, record:

* **Model**
* **Model version**
* **Environment or agent**
* **Local or cloud inference**
* **Test condition or configuration**
* **Date tested**
* **Number of follow-up prompts**
* **Manual intervention**
* **Relevant notes**

Optional information may include:

* Hardware
* Quantisation
* Context size
* Backend
* Tool configuration
* Generation time
* Token usage

## Testing Rules

To keep comparisons meaningful:

1. Every test starts with the same standard prompt.
2. The completed game must be named `classic_snake.html`.
3. The game must be completely self-contained.
4. No external dependencies are permitted.
5. The file must run directly in a browser.
6. Models should not be shown other test results before generating their version.
7. Any follow-up prompting must be recorded.
8. Any manual changes must be declared.
9. The original generated result should be preserved wherever possible.

## Contributing a Test

Community submissions are welcome.

To add your own result:

1. Run the standard prompt using the model and environment you want to test.
2. Save the result as `classic_snake.html`.
3. Create a `TEST.md` file describing the model, environment and test conditions.
4. Place both files in an appropriately named folder under `tests/`.
5. Submit the test to the repository.

A contribution might look like:

```text
tests/
└── deepseek-v4/
    └── opencode/
        └── default/
            ├── classic_snake.html
            └── TEST.md
```

## Purpose

This is not intended to be a formal scientific benchmark.

It is a practical, repeatable way to compare what AI coding systems produce when given the same small task.

The simplicity of the challenge is deliberate. Differences in implementation, design, behaviour, quality and polish are part of the test.
