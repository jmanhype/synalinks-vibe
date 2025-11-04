# AI Prompt Library

This library contains reusable prompts and patterns for AI-assisted development with Synalinks.

## Table of Contents

- [Data Model Prompts](#data-model-prompts)
- [Program Development Prompts](#program-development-prompts)
- [API Endpoint Prompts](#api-endpoint-prompts)
- [Testing Prompts](#testing-prompts)
- [Documentation Prompts](#documentation-prompts)
- [Debugging Prompts](#debugging-prompts)

## Data Model Prompts

### Create a New Data Model

```
Create a Pydantic data model for [DESCRIPTION] with the following fields:
- [field_name]: [type] - [description]
- [field_name]: [type] - [description]

Requirements:
- Include type hints for all fields
- Add Field() with descriptions for each field
- Include validation logic for [specific constraints]
- Make [field_name] optional with a default value
```

**Example:**
```
Create a Pydantic data model for a User Profile with the following fields:
- username: str - unique username for the user
- email: str - valid email address
- age: int - user's age (must be 18 or older)
- bio: str - optional biography (max 500 characters)

Requirements:
- Include type hints for all fields
- Add Field() with descriptions for each field
- Include validation logic to ensure email is valid and age >= 18
- Make bio optional with a default empty string
```

### Extend Existing Data Model

```
Extend the [MODEL_NAME] data model to include:
- [new_field]: [type] - [description]

Ensure backward compatibility and update any dependent code.
```

## Program Development Prompts

### Create a Simple Program

```
Create a Synalinks program that:
- Takes [INPUT_TYPE] as input
- Performs [OPERATION]
- Returns [OUTPUT_TYPE] as output

Use the functional API with the @synalinks.program decorator.
Include error handling for [specific error cases].
```

**Example:**
```
Create a Synalinks program that:
- Takes a Question (with question text and optional context) as input
- Uses GPT-3.5-Turbo to generate an answer
- Returns an Answer (with answer text and confidence score) as output

Use the functional API with the @synalinks.program decorator.
Include error handling for API failures and invalid inputs.
```

### Create a Class-based Program

```
Create a class-based Synalinks program for [PURPOSE] that:
- Inherits from synalinks.Program
- Accepts [PARAMETERS] in __init__
- Implements __call__ to process [INPUT_TYPE] and return [OUTPUT_TYPE]
- Includes [SPECIFIC_FEATURES]
```

### Create a Sequential Pipeline

```
Create a Sequential pipeline that:
1. [Step 1 description]
2. [Step 2 description]
3. [Step 3 description]

Each step should transform the data appropriately for the next step.
```

## API Endpoint Prompts

### Create FastAPI Endpoint

```
Create a FastAPI endpoint that:
- Route: [METHOD] /[path]
- Accepts: [REQUEST_MODEL]
- Returns: [RESPONSE_MODEL]
- Functionality: [DESCRIPTION]

Include:
- Input validation
- Error handling with appropriate status codes
- API documentation with examples
```

**Example:**
```
Create a FastAPI endpoint that:
- Route: POST /api/analyze
- Accepts: TextAnalysisRequest (text: str, analysis_type: str)
- Returns: TextAnalysisResponse (results: dict, confidence: float)
- Functionality: Analyzes text using a Synalinks program

Include:
- Input validation for analysis_type (must be one of: sentiment, entities, summary)
- Error handling with appropriate status codes (400 for invalid input, 500 for processing errors)
- API documentation with examples
```

### Add Authentication

```
Add JWT-based authentication to the [ENDPOINT_NAME] endpoint:
- Verify JWT token from Authorization header
- Extract user information
- Return 401 if unauthorized
- Include user context in request processing
```

## Testing Prompts

### Generate Unit Tests

```
Generate pytest unit tests for [FUNCTION/CLASS]:
- Test normal operation with valid inputs
- Test edge cases: [list edge cases]
- Test error handling: [list error scenarios]
- Use fixtures for [common setup]
- Mock external dependencies: [list dependencies]
```

**Example:**
```
Generate pytest unit tests for the QuestionAnswerer class:
- Test normal operation with valid Question inputs
- Test edge cases: empty question, very long question, missing context
- Test error handling: API failures, invalid model configuration, timeout
- Use fixtures for language model configuration
- Mock external dependencies: OpenAI API calls
```

### Generate Integration Tests

```
Create integration tests for [FEATURE]:
- Test end-to-end workflow: [describe flow]
- Use real [COMPONENTS] but mock [EXTERNAL_SERVICES]
- Verify: [expected outcomes]
- Clean up test data after execution
```

### Add Test Coverage

```
Analyze current test coverage for [MODULE] and add tests for:
- Uncovered functions: [list functions]
- Edge cases not currently tested
- Error paths not covered

Target: [X]% coverage
```

## Documentation Prompts

### Generate Docstrings

```
Add comprehensive docstrings to [FUNCTION/CLASS] following PEP 257:
- Brief one-line summary
- Detailed description of functionality
- Args section with type hints and descriptions
- Returns section with type and description
- Raises section for exceptions
- Example usage
```

### Create API Documentation

```
Generate API documentation for [ENDPOINT/MODULE]:
- Overview and purpose
- Request/response formats with examples
- Authentication requirements
- Error responses and status codes
- Rate limiting information
- Usage examples in [Python/curl/JavaScript]
```

### Write Tutorial

```
Create a tutorial for [FEATURE] that:
- Explains the concept clearly
- Provides step-by-step instructions
- Includes complete, runnable code examples
- Explains common pitfalls and how to avoid them
- Links to related documentation
```

## Debugging Prompts

### Debug Error

```
I'm encountering this error:
[ERROR_MESSAGE]

In this code:
[CODE_SNIPPET]

Context:
- [Relevant context]
- [What I've tried]

Please help me:
1. Identify the root cause
2. Suggest a fix
3. Explain why this error occurred
4. Recommend how to prevent it in the future
```

### Optimize Performance

```
This code is running slower than expected:
[CODE_SNIPPET]

Profile information:
[PROFILING_DATA]

Please help me:
1. Identify performance bottlenecks
2. Suggest optimizations
3. Estimate performance improvement
4. Ensure optimizations don't break functionality
```

### Refactor Code

```
Refactor this code to improve [ASPECT]:
[CODE_SNIPPET]

Goals:
- [Goal 1]
- [Goal 2]
- Maintain backward compatibility
- Keep the same functionality

Provide:
- Refactored code
- Explanation of changes
- Migration guide if needed
```

## Advanced Patterns

### Chain of Thought Reasoning

```
Create a Synalinks program that uses chain-of-thought reasoning:
- Input: [PROBLEM_TYPE]
- Output: [SOLUTION_TYPE]
- Include intermediate reasoning steps
- Provide confidence scores for each step
```

### Multi-Model Ensemble

```
Create an ensemble program that:
- Uses [MODEL_1], [MODEL_2], and [MODEL_3]
- Combines their outputs using [STRATEGY]
- Returns the most confident/consistent result
- Includes fallback logic if models disagree
```

### Iterative Refinement

```
Create a program that iteratively refines its output:
- Generate initial output
- Evaluate quality using [CRITERIA]
- If quality < threshold, refine and retry
- Max iterations: [N]
- Return best result with metadata
```

## Customization

Feel free to customize these prompts for your specific use cases. When creating new prompts:

1. **Be Specific**: Include exact requirements and constraints
2. **Provide Context**: Explain the problem and desired outcome
3. **Include Examples**: Show what good output looks like
4. **List Requirements**: Be explicit about what must be included
5. **Define Success**: Clarify how you'll know the task is complete

## Contributing

To add new prompts to this library:
1. Create a new section or add to an existing one
2. Follow the format: description, template, example
3. Test the prompt to ensure it produces good results
4. Submit a PR with your addition

## Tips for Effective AI Prompting

1. **Start Broad, Then Narrow**: Begin with high-level description, then add details
2. **Use Examples**: Show examples of inputs and expected outputs
3. **Iterate**: Refine prompts based on initial results
4. **Be Explicit**: Don't assume the AI knows your conventions
5. **Reference Context**: Point to relevant files, patterns, or documentation
6. **Break Down Complex Tasks**: Split large tasks into smaller, focused prompts
