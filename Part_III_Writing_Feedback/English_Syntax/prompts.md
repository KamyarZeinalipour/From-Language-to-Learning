# Writing Feedback Prompts

## 1. Placeholder Replacement (Privacy Preservation)
**Objective:** Restore natural flow to anonymized essays (e.g., replacing @PERSON1).

```text
Your task entails identifying and substituting placeholders within the text.
These placeholders are denoted by an '@' symbol followed by uppercase letters indicating various categories such as months, percentages, locations, numbers, person names, and more. It's crucial to ensure that the replacements seamlessly integrate into the text. Ensure that all placeholders are detected and replaced with the appropriate replacements.

To streamline the process, kindly furnish your replacements in JSON format. The JSON should comprise pairs where each placeholder is associated with its corresponding replacement word.

Text: {essay}
2. Syntax Feedback Generation
Objective: Generate structured feedback across 7 error categories.
Your task is to perform a syntax analysis on an essay, aiming to identify and amend errors across specific syntax categories. Your mission is to meticulously inspect each category for mistakes, correct them, and elucidate your findings. Concentrate on the following syntax areas:

Syntax Categories to Check:
1. Misspelled Words: Detect and list each misspelling uniquely.
2. Conjunctions and Linking Phrases: Search and list misuse of adverbs or (and, or, but, then, and because) between sentences and paragraphs.
3. Modifiers: Search for improper uses of modifiers.
4. Prepositions: Check for and correct inaccuracies in the use of prepositions.
5. Modal Verbs: Assess modal verbs for their accurate application.
6. Punctuation: Identify and rectify punctuation errors.
7. Articles: Examine the application of "the," "a," and "an," correcting any misuse.

To successfully accomplish this analysis, follow these steps:
1. Begin by systematically searching for syntax errors in the highlighted categories.
2. Ensure that you have thoroughly identified all errors...
3. If no errors are found within a specific category, indicate its absence of errors by writing "N/A" for that category.
4. Document each error found in a structured manner as follows:
   - Syntax Category [Name of Syntax Category]:
     - Error: [found error], Correct version: [appropriate correction]
   Consider that Each error should be mentioned on a separate line for clarity and order.

ESSAY: {essay}
