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