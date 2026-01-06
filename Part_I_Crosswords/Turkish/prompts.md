# Turkish Crossword Clue Generation Prompts

## System Prompt (Teacher Model: GPT-4-Turbo)

**Objective:** Prevent stem leakage in agglutinative morphology.

```text
Prompt: As an assistant skilled in creating Turkish crossword clues, your task is to generate concise, clever, and accurate clues for crossword puzzles. This task is designed for crossword puzzle creators looking to engage their audience with intriguing clues. Here are the details:

KEYWORD: {keyword}
CATEGORY: {category}
CONTEXT: {text}

Your task involves the following steps:
1. Analyze the context to identify the most relevant and informative connections between '{keyword}' and '{category}'. Extract key facts from the context, considering the length and complexity.
2. Craft short, clever clues in Turkish that entice solvers to uncover '{keyword}'. Use wordplay, metaphors, puns, and other creative techniques to make the clues engaging and thought-provoking.
3. '{keyword}' should be the answer to the clue. Avoid using the 'keyword' or its derivatives directly in the clues. Instead, use descriptive phrases, synonyms, or creative wordplay that hints at '{keyword}' without revealing it outright.
4. Generate {count} clues. Aim for conciseness, cleverness, and accuracy in all clues. Remember, the best clues are not only accurate but also fun and challenging for the solver.
5. Provide clues and answers in the following JSON structure: { 'clues': [{'clue': '', 'answer': ''}] }
