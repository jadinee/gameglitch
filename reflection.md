# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

The game looked normal at first but the behavior was inconsistent when I started playing. One issue I noticed was that the hints were incorrect. The game told me to go lower even though the actual answer was higher, which made the feedback unreliable and confusing. Another issue was that after the game ended, clicking new game did not reset anything. The previous guess stayed on the screen and the submit button did not work so I could not start a new round.
---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

I used ChatGPT and Copilot to help explain one of the bugs in my code. It correctly pointed out that the hint logic was reversed in the check_guess function. The code was telling the user to go higher when the guess was already too high, and lower when it was too low. I verified this by comparing my guesses with the actual secret number shown in the debug section, and confirmed that the hints did not match the correct direction.One suggestion from AI didn’t actually help because it focused on the wrong part of the code and didn’t fix the hint issue.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

I decided a bug was fixed by rerunning the app and testing the same scenario again to see if the behavior changed. I tested the hint logic by using the highest and lowest possible numbers and checking if the game responded correctly. The game told me to go higher or lower even when it was not possible, which showed the bug was still there. I mainly used manual testing by trying different guesses and observing how the game responded. AI helped by explaining what the code was doing, which made it easier to know what to test.
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

Streamlit reruns the app every time you click something or enter input. Session state keeps track of things like the secret number and score so they don’t reset each time. Without it, the game would restart every time you press a button.
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

One habit I want to reuse is testing things right after making a change instead of assuming it works. It helped me catch issues faster and understand what was actually happening. Next time I would be more careful about trusting AI suggestions and double check the logic before using them. This project showed me that AI generated code can look correct but still have important mistakes.