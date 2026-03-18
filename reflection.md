# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
1. The game always ends with one attempt left. I expected to use all of my 8 attempt but only used 7.
2. The game's hint was inaccurate. It would say higher or lower, so I expected the output to be inbetween, however, it was completely outside of the bound.
3. When the game ends and you press new game, it does not load a new game

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
- I used a combination of Github Copilot and Claude. Since both of my agent was free tier, I had limited queries.
- One suggestion that was correct was when the guess was greater, it displayed higher, do the ai reversed the logic and the print statement. I have verified the result by running the app on the web.
- One AI suggestion that was misleading was when I asked it about how the game ends even when it display one attempt left. The AI fixed the counter but it added another mistake, which was it did not display reduced attempts for the first try--instead it showed 8 attempts after the first guess.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I used pytest to see if it passes the test as instructed, but more importantly I saved the file and played it again to see if it was fixed.
- Describe at least one test you ran (manual or using pytest)
  and what it showed you about your code.
I tested whether the fame ended at 0 or 1 attempt, which failed multiple time.
- Did AI help you design or understand any tests? How?
AI helped set up everything for the pytest and I only needed to run the command to test it in terminal

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

Streamlit basically works by rerunning your whole script everytime someone interacts with the app, like clicking a button or something. It might feel a bit wierd at first because everything resets each time, but thats just how it updates the UI. To save everything before it restart everytime, you just use st.session_state to keep all the important memory.
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
I would probably try to use inline suggestion that Github has, but unfortunately it has a limit for free users.
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  I will use pytest to efficiently test my code in the future
- What is one thing you would do differently next time you work with AI on a coding task?
I would tell the agent first the type of problem I  am dealing with so that it could locate it. Then I will ask it to explain the code and what it does. Then I will ask it to explain what is wrong and provide a suggested code that can fix the logical problem.
- In one or two sentences, describe how this project changed the way you think about AI generated code.

Although AI generated code is good, if you purely rely on it, you will not understand your code it all. Furthermore, it might get the job done--however it will neither be efficient or fast.