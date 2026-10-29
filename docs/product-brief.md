# Product brief

## The problem

Entry-level jobs in India, such as telecalling, customer support, retail sales, back office and reception, often ask for "basic" or "good" English. Many people applying for them think in Hindi or another Indian language. Only about 1 in 10 Indians speaks any English (Census 2011).

These job seekers usually understand simple English. What they can't yet do is make an English sentence on the spot, under pressure, which is what an interview tests. They also feel nervous speaking, and embarrassment makes people stop practising.

Existing English apps teach general vocabulary, and many are built around reading or tapping rather than speaking. They don't teach the handful of words a specific job uses every day, such as *escalate* for a telecaller or *out of stock* for a retail associate.

## The learner

**Primary learner (a composite persona):** Pooja, 22, a graduate from a Hindi-speaking city. She understands simple English but hesitates to speak it. She wants a customer support or front-office job, and practises on her phone in breaks of 5 to 10 minutes.

**Secondary learner:** an English-comfortable graduate who wants to sharpen job-specific vocabulary. They use English mode.

## Which jobs

A role family made version 1 only if it is high-volume for entry-level job seekers **and** its listings ask for English. In a sample of 59 live entry-level listings on a large Indian jobs platform (October 2026):

- all 9 telecalling listings were tagged "Basic English" or "Good English";
- 33 of 38 delivery listings said "No English required", so delivery was left out.

Version 1 covers four role families, with 12 words each: telecalling and customer support, sales and retail, back office and data entry, and front office and reception. Every word comes with a simple meaning, a Hindi meaning, a work sentence, and a common mistake Indian English speakers make with it.

## Scope of version 1

**In:**
- Voice sessions of about 5 minutes, 5 words each.
- Hindi-led explanations with English practice, or English throughout.
- A three-step ladder per word: repeat, change one part, own sentence.
- Whole-sentence feedback with one more try per step.
- A spoken recap and a goodbye; the tutor ends the call itself.
- A public link that works in a browser, with typing as a fallback.

**Out, for later versions:**
- Pronunciation scoring. The model receives a transcript, not the voice.
- Progress saved across sessions, and spaced repetition of words a learner found hard.
- Other Indian languages.
- More role families and longer word lists.

## Session design

The design follows three ideas:

1. **Explain in the language the learner thinks in, practise in English.** Every instruction and piece of feedback is in simple Hindi in Hindi mode, from the greeting to the goodbye. The words, the work sentences and everything the learner says are in English.
2. **Build up to speaking, don't start with it.** Making a sentence from nothing is where a nervous speaker stalls. The ladder starts with repetition, then a guided change, and asks for an own sentence only when the learner is ready.
3. **Short turns, one question at a time.** Long spoken replies feel like a lecture and add delay.

## How success would be measured

For a prototype:
- every session that reaches the close ends with the tutor ending the call;
- at least 9 of every 10 right-or-wrong judgements on the learner's sentences are correct;
- sessions finish in under 7 minutes;
- reply delay stays under about 2 seconds;
- all guardrail tests pass.

For a product, inside a jobs platform:
- **Primary:** the interview-to-hire rate of learners who used the tutor before an interview for a job that asks for English, against a group who were not offered it.
- **Secondary:** the share of learners who come back for another session within 7 days.
- **Guardrail:** cost per session stays within a set budget.

## Risks

| Risk | How it is handled |
|---|---|
| The tutor mis-hears the learner's English sentence in Hindi mode | The 48 work words are given to speech recognition as keywords. If mis-hearing persists, the fallback is an English call with Hindi explanations. |
| Wrong feedback teaches wrong English | A fixed word list with known common mistakes, a whole-sentence check, and a test plan that checks right-or-wrong judgements |
| A nervous learner gives up | The three-step ladder, a limit of two tries per step, and no pushing when the learner says they can't make a sentence |
| A public link is misused | Built-in guardrails, prompt-level rules, and a 7-minute cap on every call |
