Test Date: 2025-06-12.

Test Platform: [SIDER AI](https://sider.ai/).

Prompt: `9.11 - 9.9 = ?` and `9.9 - 9.11 = ?`.


# The Mystery of Zero Point Two One

1. Some well-known large language models, including Claude 4 Opus, when asked “9.9 - 9.11 = ?”, will answer **-0.21**.
2. Non-reasoning models almost all get **-0.21**, and even reasoning models often arrive at **-0.21** in their chain of thought.
3. Clearly, companies have fine-tuned their models—some will first answer **-0.21**, then correct themselves to **0.79**.
4. I also tried “9.11 - 9.9 = ?”, and they answer **0.21**.
5. Tokenizer can not be the reason. I do not believe these companies are using the same tokenizer.
6. So why does it calculate **-0.21**? Even if the model interprets the numbers as dates or version numbers, the result should be **-0.20**, not **-0.21**.
7. Findings: https://github.com/Physics-Lee/Why_Zero_Point_Two_One

# The Mystery of Zero Point Two One | Part 2

1. For Part 1, check https://github.com/Physics-Lee/Why_Zero_Point_Two_One
2. Today, I use API to test this mystery. When using API, the LLM will not the history of our chatting.
3. For each question, I test 5 times.
4. For `i.11-i.9` `9.i1 - 9.9` `9.11-9.i` `9.1i-9.9`, they will make mistakes sometimes, never answer it right every time. 
5. For `39.1i - 29.9` and `4929.1i-5929.9`, they give the right answer every time.
6. Final thought: For machines, the human language is not language, just a high dim distribution. If do further research, I will start from below two methods:
   1. Use Diffusion Language Models (like [Google Diffusion](https://deepmind.google/models/gemini-diffusion/)), instead of auto-regressive language models, to conduct the same research.
   2. Enlarge the range of the computation. Like `abcd.efg - hijk.lmn`, each character loop from 0 to 9.