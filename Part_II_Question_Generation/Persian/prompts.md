# Persian MCQ Generation Prompts (3-Stage Cascade)

## Stage 1: Text Augmentation
**Objective:** Transform raw text into an argumentative passage.

```text
As an Educational Assistant your role is to transform the given Persian text into an argumentative passage, supporting a specific viewpoint and main topic with relevant evidence. Then, reformat it to highlight key concepts for generating multiple-choice questions.

1. Transform the original text into an argumentative passage.
2. Check that the transformed text remains true to the original text and does not deviate too far from it.
3. Ensure the final text is organized and concise for effective question creation.
4. Proofread for grammar and spelling.
5. Ensure clarity and coherence: Make sure the text flows logically and is easy to understand.
6. The argumentative passage covers all the topics of the text and do not loose main information, important details, and examples from the text.

The output should be a concise well-structured text in Persian. I just need the argumentative passage as an output, nothing else.

TEXT: {original_text}
Stage 2: MCQ Generation
Objective: Generate initial draft of questions.
As an Educational Assistant, your role is to generate multiple-choice questions in Persian from the given text. Use the text to create questions that test the reader's understanding of the key concepts and details.
[...Instructions on components: stem, correct answer, distractors...]

1. Identify key concepts and details in the text.
2. Create clear, concise, and relevant multiple-choice questions and the question exists directly in the text.
3. Ensure each question has four answer choices, with one correct answer and three distractors.
4. Make sure the correct answer exists directly in the text and is true.
5. Make sure the question is grammatically correct in Persian...
[...Additional constraints on distractors, length, and repetition...]

Each string in the list should follow this format:
1. The first line contains the main question text.
2. The subsequent lines contain the answer options...
3. Correct questions should always be the first choice in الف.

TEXT: {first_step_text}
Stage 3: MCQ Refinement
Objective: Increase complexity and pedagogical value.
As an Educational Assistant, your role is to increase the complexity of the three multiple-choice questions that you receive as input, using the text for this purpose.

1. For each question, make the structure of question more complex, requiring careful analysis and deeper thought...
2. Ensure that the correct answer and the three distractors are more nuanced...
3. The correct answer and three distractors should be more complex in content and structure...
4. Incorporate common misconceptions or similar terminology to test deeper understanding.
[...Additional constraints on grammar and plausibility...]

TEXT: {first_step_text}
Multiple-Choice Questions: {second_step_text}
