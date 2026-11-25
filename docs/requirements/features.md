# Features

Code Coach is a web application, run on your own computer, that coaches you through coding interview problems: the kind found on LeetCode, NeetCode and HackerRank. The aim is to review problems quickly and deeply enough that these exercises become routine and you come across as a strong hire in any coding interview. The screen is split in two: a code editor on the left where you solve the problem in Python, Java, TypeScript, Rust or Go and run it against test cases, and a chat on the right that presents the problem, answers questions, gives hints and teaches. The chat is powered by a local LLM, seeded with high quality teaching content prepared with Claude.

History: items 1 to 23 are the first list (the owner, 2026-11-24). The owner answered the open questions on problem sources, the local LLM, Docker and platforms on 2026-11-25.

Items marked *(default)* are choices made on the owner's behalf, pending confirmation.

## Layout

1. **Two-pane screen.** The application shows the code editor on the left half and the chat on the right half of the browser window.
2. **Resizable panes.** You can drag the divider between the panes to give either side more room. *(default)*

## Problems

3. **Problem list.** You can browse the available problems and pick one to work on. Each shows its title, difficulty and the concept it teaches (for example two pointers, graphs, dynamic programming). *(default)*
4. **Problem sources.** Problems are modelled on the problem types found on LeetCode, NeetCode, HackerRank and other coding exercise sites, but their text is never copied. Each problem is either our own variation of a known problem type or a public domain version of it. What matters is that it matches the original's difficulty, the type of solution and the concept learned by solving it. *Decided by the owner, 2026-11-25: copying the sites' problem text and tests was rejected because their terms forbid it and the text is copyrighted.*
5. **Problem contents.** Each problem has a statement, examples, constraints, the function signature to implement in each supported language, and a set of test cases.
23. **What each problem teaches.** Each problem records its difficulty, the type of solution it needs (for example sliding window or breadth-first search) and the concept learned, so the coaching can focus on the idea rather than on one specific problem. (the owner, 2026-11-25)

## Chat

6. **Presents the problem.** When you open a problem, the chat presents it: the statement, the examples and the constraints.
7. **Answers questions.** You can ask the chat questions about the problem or about any coding topic (a data structure, an algorithm, a language feature, time and space complexity) and it explains.
8. **Hints on request.** When you ask for a hint, the chat gives one. Hints start small and get more specific each time you ask, so you can stop as soon as you are unstuck, without being handed the full solution. *(default)*
9. **Sees your work.** The chat can see your current code and your latest test results, so its answers and hints fit where you actually are. *(default)*
10. **More chat features later.** The chat will be refined over time; this list covers the first version.

## Code editor

11. **Five languages.** You can write your solution in Python, Java, TypeScript, Rust or Go, and switch language from the editor.
12. **Starter code.** When you pick a problem and a language, the editor fills in the function signature for that language.
13. **Editor basics.** The editor has syntax highlighting, line numbers and auto-indent for each language. *(default)*
14. **Keeps your code.** Your code for each problem and language is kept, so leaving and coming back doesn't lose it. *(default)*

## Running and testing

15. **Run against tests.** You can run your code against the problem's test cases with one button.
16. **Results per test.** After a run you see which tests passed and which failed, and for a failed test, the input, the expected output and what your code returned.
17. **Program output.** You see everything your code printed, including debugging output you added, and any compile or runtime error with its message.
18. **Overall verdict.** Each run ends with a clear verdict: all tests passed, some failed, it didn't compile, it crashed, or it ran too long. *(default: a run that takes more than 10 seconds is stopped)*
19. **Your own test cases.** You can add test cases of your own and run them alongside the problem's. *(default)*

## Local LLM and teaching content

20. **Local LLM.** The chat runs on an LLM installed on your own computer through Ollama, so it works without a paid API. It must run well on a laptop with 16 GB of RAM and no GPU. The model is the one that works best for this chat on that machine, picked by trying a few candidates and written up as an experiment. *Decided by the owner, 2026-11-25: Ollama. Which model is still open; the first candidates are 7B to 8B coding and instruction models.*
21. **Seeded by Claude.** Each problem comes with teaching content prepared ahead of time with Claude: the key idea, a ladder of hints, common mistakes, an explained solution and its complexity. The local LLM draws on this content so its answers are accurate and high quality.

## Running locally

22. **Runs on your computer.** The whole application runs locally on your laptop and is opened in a web browser. Your code runs inside Docker, so one install covers all five languages and runaway code can't harm your machine. The first version runs on Windows only. *Decided by the owner, 2026-11-25: Docker was chosen over installing each language's tools directly on the machine.*
