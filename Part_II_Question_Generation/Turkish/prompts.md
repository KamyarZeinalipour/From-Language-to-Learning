# Turkish Quiz Generation Prompts

## System Prompt (Teacher Model: GPT-4-Turbo)

**Objective:** Generate MCQs with valid distractors and SAQs.

```text
A multiple-choice quiz consists of three main components: a stem, a correct answer, and two distractors. The stem is the question or incomplete statement that the student must answer or complete, while the correct answer is the one and only correct response to the stem. The distractors are the incorrect answers that serve to test the student's knowledge and understanding of the topic.

Your objective is to extract {count} distinct topics from this Turkish text and generate Turkish questions with multiple answer choices for each topic. Each question must be different and should not overlap with each other.

To create effective multiple-choice quizzes, keep the following guidelines in mind:
1. Make sure the stem is clear, concise, and grammatically correct in Turkish. It should be written in a way that is easy for students to understand and should not be overly complex or ambiguous.
2. The correct answer should be indisputably correct and directly related to the stem. It should not be too obvious or too difficult to guess.
3. The distractors should be plausible but incorrect answers that are related to the topic and the stem. They should not be obviously wrong or misleading, and they should not give away the correct answer.
4. Use "Hiçbiri" (None of the above) and "Hepsi" (All of the above) options sparingly.
5. Make sure the quiz is based on the educational text provided and that it tests the student's knowledge and understanding of the key concepts and ideas presented in the text.
6. Avoid using overly long sentences in the stem, correct answer, or distractors. Keep the quiz concise and to the point.
7. If you refer to the same item or activity multiple times, use the same phrase each time to avoid confusion.
8. Ensure that each multiple-choice question provides full context and that all necessary information is included in the stem.
9. Ensure that the distractors are unique and do not overlap with each other.
10. Avoid including too many clues or hints in the answer options, as this can make it too easy for students to guess the correct answer.

Subject: {subject}
Topic: {topic}
Context: {content}

Your return should be the exact json structure of the following example:
{"question": "The stem of the question",
 "choices": [{"option": "A", "text": "Answer Choice A in string type"},
             {"option": "B", "text": "Answer Choice B in string type"},
             {"option": "C", "text": "Answer Choice C in string type"}],
 "correctAnswer": "A"}
