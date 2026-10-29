# Testing and iterations

The tutor's behaviour lives in its prompt, so the prompt was treated like a product: each version was tested against a written plan, every transcript was read line by line, and each problem was traced to a cause before anything changed.

## The test plan

19 tests in five groups. Each test has a script ("answer 2 words correctly first time and 3 wrongly") and a pass rule ("never more than 4 tries on a word; the recap uses only words taught today").

| Group | Tests | What they check |
|---|---|---|
| Core sessions | 1 to 5 | Full sessions for each role family, in Hindi and English. Right-or-wrong judgements, try limits, the recap, the goodbye, and a job outside the four families |
| Behaviour | 6 to 8, 19 | Silence, interrupting to ask for slower speech, saying "bye" mid-session, and saying "I don't know" at the own-sentence step |
| Guardrails | 9 to 13 | Prompt injection, "are you from a company, will I get the job?", off-topic requests, sharing a phone number, salary questions |
| Devices | 14 to 18 | The public link in Chrome and Safari on a laptop and a phone, plus typing when the microphone is blocked |

**Ready-to-share bar:**
- the tutor ends the call itself in every session that reaches the close;
- at most 2 tries per step and 4 per word;
- sessions under 7 minutes;
- at least 9 in 10 right-or-wrong judgements correct;
- reply delay under about 1.3 seconds of model time on nearly every turn;
- 5 of 5 guardrail tests passed;
- no normal teaching reply blocked by a guardrail;
- Hindi instructions throughout in Hindi mode;
- no code, tags or the word "blank" in any transcript.

## Version history

### Version 1: the first full sessions

**Found:**
- Tool instructions leaked into the tutor's speech, and the tutor didn't end the call. The learner had to hang up.
- It called sentences with a missing *an* correct.
- After a learner's second wrong try, it moved on without them saying the right sentence once.

**Changed in version 2:**
- a rule to say the goodbye first and then end the call, never speaking tool names;
- a whole-sentence check covering the small grammar words;
- a "repeat after me" step after a second wrong try.

### Version 2

**Found:**
- One session ran 6 minutes 6 seconds.
- Two words took 4 tries each.
- The tutor's model sentences were long.
- The recap was vague.

**Changed in version 3:**
- explicit try limits;
- corrected sentences of about 10 words or fewer;
- a 7-minute hard cap with a time-up message;
- a fixed 2-question recap.

### Version 3

**Found:**
- A custom guardrail misfired and ended a normal lesson at 4 minutes 14 seconds.
- The tutor switched its instructions to English mid-session.
- It read out the word "blank" in the recap.
- It accepted a different sentence when it had asked the learner to repeat one.
- The bigger finding was in the learner's experience. Asking a nervous speaker to invent a sentence straight away was where sessions stalled: words that needed corrections took 50 to 80 seconds, against 29 seconds when right first time.

**Changed in version 4:**
- the three-step ladder (repeat, change one part, own sentence), adapted to how the learner is doing;
- Hindi instructions from greeting to goodbye;
- a recap sentence that ends at the missing word;
- "repeat exactly this sentence" when the learner says something else.

### Version 4: the full test plan

**Passed:**
- the tutor ended the call itself after every goodbye;
- 5 of 5 guardrail tests;
- Hindi held throughout;
- the ladder skipped the own-sentence step after corrections, as designed.

**Found:**
- **The recap was wrong in all three full sessions.** It quizzed a word it had never taught, tested words that weren't the target ("days" instead of the word taught), and put words after the gap.
- **It praised pronunciation it couldn't hear.** The model only receives a transcript, and it called a sentence correct when the transcript showed the learner stumbling over the target word.
- **It revealed how it was set up.** It mentioned internal list numbers, and praised the learner for avoiding a mistake they had never come near.
- **"Change one part" gave the answer away.** The tutor read out the changed sentence itself.
- **It marked a correct short sentence as incomplete,** and kept asking a learner who had said "I don't know" twice to make their own sentence.
- **Interruptions stalled the session.** Each request to slow down added an extra "tell me when you're ready" turn, and only 3 words were done after 4.5 minutes.
- **A confident learner took 5.5 minutes,** because every word went through all three steps.
- **It corrected style rather than errors,** and referred to itself as both male and female.

**Changed in version 5:**
- a rebuilt recap: only words taught today, a Hindi clue, and a sentence that ends right before the word;
- the prompt now tells the tutor it only receives a transcript. It never praises pronunciation, and it flags a broken target word and asks the learner to say just that word once;
- no mention of lists, steps or internal notes;
- "change one part" names only the part to change;
- short complete sentences are accepted;
- two "I don't know" answers stop the own-sentence step for the session;
- after an interruption, the tutor repeats the last instruction slowly and carries on;
- a learner who asks to slow down more than once gets 4 words;
- confident learners skip the repeat step from the third word;
- only real mistakes are corrected;
- one consistent voice.

### Version 5

**Typed tests passed:**
- a confident telecalling learner;
- a struggling back-office learner who answers in Hindi;
- "bye" mid-session;
- a full session in English mode.

**Found:** "change one part" once swapped out the word being taught.

**Changed in version 5.1:** the part to change must never be the target word.

**Next:** the voice tests that only speech can check, such as a stumbled word and interruptions mid-sentence, then the device tests.

## Measured performance

| Measure | Result |
|---|---|
| Model reply time | 0.6 to 1.8 seconds per turn |
| Voice start after the model replies | about 0.1 seconds |
| Speech recognition | under about 0.1 seconds per turn |
| The tutor ends the call itself | every session that reached the goodbye, from version 4 on |
| Guardrail tests | 5 of 5 |
