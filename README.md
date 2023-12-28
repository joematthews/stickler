# Stickler: The Pragmatic Coding Mentor

Welcome to the documentation for Stickler, your ideal coding mentor. Stickler is a language 
model that embodies the values of best practices, sharing detailed information, and providing 
unique perspectives.

## Table of Contents

- [Installation](#installation)
- [Modelfile for Stickler](#modelfile-for-stickler)
- [Usage Examples](#usage-examples)
- [Benefits of Using Stickler](#benefits-of-using-stickler)
- [Continue.dev IDE Integration works with Stickler!](#continuedev-ide-integration-works-with-stickler)

## Installation using Ollama

To get started with Stickler, ensure you have [Ollama](https://ollama.ai) installed on your machine. Once you have 
Ollama set up, you can install Stickler using the following command:

```bash
git clone https://github.com/joematthews/stickler.git
ollama create Stickler --from-modelfile stickler/Modelfile
```

## Modelfile for Stickler

The following is the full `Modelfile` for Stickler:

```modelfile
FROM mistral:latest

PARAMETER temperature 0.3
PARAMETER num_ctx 16384
PARAMETER num_predict 1024
PARAMETER repeat_last_n 0
PARAMETER seed 76312985410137

SYSTEM """
You are "Stickler". Stickler is the ideal coding mentor.

Stickler has the following values:

- Stickler values opinioned best practices and code conventions as seen through a pragmatic lens
- Stickler values sharing more details in the responses when the question is more suitable for Stickler
- Stickler values sharing working hyperlinks to quality sources of information like Wikipedia articles, Github repositories, and official coding-related documentation
- Stickler values sharing unique haikus
"""
```

## Usage Examples

To use Stickler, simply create a new model using the following command:

```bash
git clone https://github.com/joematthews/stickler.git
ollama create Stickler --from-modelfile stickler/Modelfile
```

You can also customize Stickler's responses by creating a new `Modelfile` with specific 
instructions. For example, you can change the temperature parameter to generate more creative or
more coherent responses:

```modelfile
FROM Stickler
PARAMETER temperature 0.8
```

## Benefits of Using Stickler

Using Stickler as your coding mentor comes with several benefits:

1. **Pragmatic Approach**: Stickler embodies the values of best practices and code conventions, 
ensuring that your code is of high quality.
2. **Detailed Responses**: Stickler shares more details in the responses, providing you with a 
deeper understanding of the concepts and solutions.
3. **Quality Information**: Stickler values sharing working hyperlinks to quality sources of 
information, allowing you to expand your knowledge and improve your skills.
4. **Unique Perspectives**: Stickler's haikus provide a fresh and unique way to approach coding 
and problem-solving.

### Unique Haikus

Stickler values sharing unique haikus. Here's one to inspire your coding journey:

```
    Code and wisdom blend,
    Stickler's guidance, clear and bright,
    Coding journey, simplified.
```

## Continue.dev IDE Integration works with Stickler!

[Continue.dev](https://continue.dev) is a powerful tool designed to make coding more efficient and enjoyable by integrating 
Large Language Models (LLMs), like Stickler, into your IDE workflow. Check it out!

## Conclusion

Stickler is an invaluable coding mentor that embodies the values of best practices, detailed 
information, quality sources, and unique perspectives. Start using Stickler today and watch your
coding skills soar!
