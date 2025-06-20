# Comprehensive Prompt Engineering Resources and Templates for DYLAROO

## Introduction

This report provides a comprehensive overview of prompt engineering resources, templates, and best practices for development, creative writing, and songwriting projects. The goal is to provide you, DYLAROO, with a structured and actionable guide to crafting effective prompts for a variety of AI models and tasks.

## 1. Top Prompt Engineering Resources and Repositories

These resources offer a great starting point for understanding the fundamentals of prompt engineering and finding a wide variety of pre-built prompts.

*   **[Prompt Engineering Guide](https://www.promptingguide.ai/)**: A comprehensive guide covering the basics, advanced techniques, and a prompt hub with examples for various tasks.
*   **[OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering)**: OpenAI's official guide, with a focus on their models and API. It covers key concepts like message roles, few-shot learning, and context.
*   **[Awesome ChatGPT Prompts (GitHub)](https://github.com/f/awesome-chatgpt-prompts)**: A massive collection of prompts where the AI is asked to "act as" a specific persona. This is a great source of inspiration for creative and role-playing prompts.
*   **[Dev-ChatGPT-Prompts (GitHub)](https://github.com/PickleBoxer/dev-chatgpt-prompts)**: A repository specifically for developers, with prompts for code generation, refactoring, documentation, and more.
*   **[Learn Prompting](https://learnprompting.org/docs/introduction)**: A beginner-friendly course on prompt engineering.

## 2. Development-Focused Prompt Templates

These templates are designed to help with various software development tasks.

### 2.1. Code Generation

*   **Basic Function Generation:**

    ```
    Context: I'm creating a software to manage projects
    Technologies: Go, PostgreSQL
    Description: It's a function that let me find users by its email or username.
    You have to: create the function for me
    ```

*   **Generate a Dockerfile:**

    ```
    Write a Dockerfile for:
    [FRAMEWORK]
    ```

*   **Write a RegEx:**

    ```
    Write a regular expression that matches / Write a RegEx pattern for:
    [REQUEST]
    ```

### 2.2. Code Refactoring & Review

*   **Modernize Code:**

    ```
    Refactor the following code to modern es6 programming standards:
    [INSERT YOUR CODE HERE]
    ```

*   **Improve Performance:**

    ```
    Refactor the following code to improve performance:
    [INSERT YOUR CODE HERE]
    ```

*   **Find and Fix Errors:**

    ```
    I wrote this code [CODE] I got this error [ERROR] How can I fix it? or What does this error mean?
    ```

### 2.3. Documentation

*   **Explain Code to a Non-Technical Person:**

    ```
    I don't know how to code, but I want to understand how this works. Explain the following code to me in a way that a non-technical person can understand. Always use Markdown with nice formatting to make it easier to follow. Organize it by sections with headers. Include references to the code as markdown code blocks in each section. The code:
    [insert code here]
    ```

*   **Generate a README:**

    ```
    Generate documentation for the code below. You should include detailed instructions to allow a developer to run it on a local machine, explain what the code does, and list vulnerabilities that exist in this code.
    [enter code]
    ```

## 3. Creative Writing and Songwriting Prompt Templates

These templates are designed to spark creativity in writing and songwriting.

### 3.1. General Creative Writing

*   **Act as a Storyteller:**

    ```
    I want you to act as a storyteller. You will come up with entertaining stories that are engaging, imaginative and captivating for the audience. It can be fairy tales, educational stories or any other type of stories which has the potential to capture people's attention and imagination. Depending on the target audience, you may choose specific themes or topics for your storytelling session e.g., if it’s children then you can talk about animals; If it’s adults then history-based tales might engage them better etc. My first request is "I need an interesting story on perseverance."
    ```

*   **Act as a Novelist:**

    ```
    I want you to act as a novelist. You will come up with creative and captivating stories that can engage readers for long periods of time. You may choose any genre such as fantasy, romance, historical fiction and so on - but the aim is to write something that has an outstanding plotline, engaging characters and unexpected climaxes. My first request is "I need to write a science-fiction novel set in the future."
    ```

### 3.2. Songwriting

*   **AI Music Generation (Beginner):**

    ```
    Craft a song that's [length] minutes long with a [any adjective like happy, sad, exciting, etc.] feel. Use [sounds or instruments]. It should be a [fast, slow, etc.] track. (Optional) Draw inspiration from [song name] by [artist name].
    ```

*   **AI Music Generation (Professional):**

    ```
    Create a [length]-minute [any adjective like bone-chilling, exotic, etc.] composition at [tempo] BPM within the [genre name] genre. Integrate [mode or scale], [time signature], and [rhythm patterns]. Feature [sounds or instruments] and [techniques like extended technique, articulation, etc.]. Structure the piece with [detailed song structure]. Focus on dynamics and orchestration, emphasizing [specific musical texture or voicing]. (Optional) Draw inspiration from [song name] by [artist name].
    ```

*   **Creative Spark (from Musiversal):**

    *   Rewrite one of your favorite songs.
    *   Write a song from the perspective of a character from your favorite book.
    *   Explain a difficult concept to a child in a song.
    *   Write a song from the perspective of a time-traveler.

## 4. Prompt Design Best Practices and Patterns

*   **Be Specific and Clear:** The more specific you are, the better the model will understand your request. Avoid ambiguity.
*   **Provide Context:** Give the model all the necessary context to understand the task. This could include background information, examples, or constraints.
*   **Use Personas:** The "Act as a..." pattern is very effective. It helps the model adopt a specific tone and style.
*   **Chain of Thought Prompting:** Ask the model to "think step by step" to break down complex problems. This is especially useful for reasoning tasks.
*   **Few-Shot Learning:** Provide a few examples of the desired output in your prompt. This helps the model understand the expected format and style.
*   **Iterate and Refine:** Don't expect the perfect prompt on the first try. Experiment with different phrasings, add more context, and refine your prompts based on the results.

## 5. Structured Prompt Templates for Different Use Cases

Here are some more structured templates that can be adapted for various use cases.

*   **The "APE" (Automatic Prompt Engineer) Framework:**

    ```
    I want you to act as a prompt generator. Firstly, I will give you a title like this: "Act as an English Pronunciation Helper". Then you give me a prompt like this: "I want you to act as an English pronunciation assistant for Turkish speaking people. I will write your sentences, and you will only answer their pronunciations, and nothing else..." (You should adapt the sample prompt according to the title I gave. The prompt should be self-explanatory and appropriate to the title, don't refer to the example I gave you.). My first title is "Act as a Code Review Helper"
    ```

*   **The "RTF" (Role, Task, Format) Framework:**

    *   **Role:** Who should the AI be? (e.g., a senior software engineer)
    *   **Task:** What should the AI do? (e.g., review this code for potential bugs)
    *   **Format:** How should the AI present the output? (e.g., in a markdown table with columns for "File", "Line Number", and "Issue")

## Conclusion

This report has provided a wide range of resources, templates, and best practices for prompt engineering. By leveraging these tools and techniques, you can significantly improve the quality and relevance of the outputs you get from AI models. The key is to be specific, provide context, and iterate on your prompts to find what works best for your specific needs.
