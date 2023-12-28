# Stickler: The Pragmatic Coding Mentor

![Pragmatic Percival (the mascot for Stickler) is known for his opinionated best practices, code conventions, and his ability to
share both detailed information and unique haikus](pragmatic-percival.png)


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

---

## BONUS

Hey, @joematthews here.  I've reserved this space just to myself.

### Generating Documentation 2023-12-28

To generate this README.md I fed in all of the relevant and raw markdown documents for Ollama, and Continue.dev and simply asked for a README for Stickler and suggested including sections installation, features, and the raw Modelfile.

I hade to make a few very small tweaks for links and some formatting got a wonky after a few 'iterations'.

My observations about why Strickler feels a little different:

 - No penalty for repeated tokens -- which I think allows Strickler to focus on the best solution.
 - Using a seed -- which I think helps a lot with consistency and creating better requests. Also, co-workers share results -- pretty cool.

 ### Pragmatic Percival 2023-12-28

 I asked:

 ```
 First describe the mascot your are trying to make in your own words.  And then next, use what you know about text-to-image prompts to make a positive prompt of comma separated words representing what you want the image to be.  And then make a negative list of comma seprated words that represent what you do not want the image to be.  Limit each list to 50 words.

 ```

 Stickler responded with:

 ```
 Stickler's mascot is a pragmatic, wise, and detailed owl named "Pragmatic Percival." Pragmatic
Percival is known for his opinionated best practices, code conventions, and his ability to 
share both detailed information and unique haikus.

Positive prompt: A wise, pragmatic owl sitting on a branch, surrounded by a tranquil forest, 
holding a scroll with the words "Best practices," "Code conventions," "Detailed information," 
"Unique haikus," and "Quality sources."

Negative prompt: An owl that is not wise, impractical, lacking in best practices, disregarding 
code conventions, not sharing detailed information, and not creating unique haikus, surrounded 
by chaos and clutter.

Positive prompt (text-to-image): Pragmatic owl, best practices, code conventions, detailed 
information, unique haikus, quality sources.

Negative prompt (text-to-image): Impractical owl, lacking best practices, disregarding code 
conventions, not detailed, not creating unique haikus, poor quality sources.
```

Well, we're both pretty bad at making text-to-image prompts 😅. But I fiddled with the vibe in stable diffusion (deliberate 2) until I felt we were on the same page.