# Agent settings

The tutor runs on ElevenLabs Agents with no custom code. These are the settings that shape its behaviour, with the reason for each.

## Language and voice

| Setting | Value | Why |
|---|---|---|
| Default language | Hindi | Most learners this is built for think in Hindi. Explanations they understand come first; the practice itself is always in English. |
| Additional language | English | For learners who are comfortable in English, and for reviewers who don't speak Hindi. The learner picks the language before the call. |
| Language detection | Off | If it were on, a learner in Hindi mode saying an English practice sentence could switch the whole call to English. |
| Hindi voice | A warm Hindi voice with an Indian accent | Chosen by listening to a mixed sentence and checking that English work words sound clear. |
| English voice | An Indian English voice | Familiar to the learner and closer to what they will hear at work. |

## Model

| Setting | Value | Why |
|---|---|---|
| Language model | Claude Opus 4.7, with GPT-5.6 Terra as backup | The tutor has to follow a long prompt, write Hindi in Devanagari next to English words, and judge English sentences correctly. Smaller models fail first on exactly these. Reply speed was measured on test calls and stayed between 0.6 and 1.8 seconds per turn. |

## Conversation

| Setting | Value | Why |
|---|---|---|
| Speech recognition | Realtime, with 48 keywords (the work words) | The keywords help the transcript spell the work words correctly. The side effect: a slightly wrong pronunciation can still be written as the right word. |
| Prompt the learner after silence | 10 seconds | The tutor asks once whether the learner is still there and repeats the question more simply. |
| End the call after silence | 30 seconds | A call left open would keep running. |
| Maximum call length | 420 seconds (7 minutes), with a time-up message | A session is designed for about 5 minutes. The cap leaves room for a slow learner and still stops a call left open. |
| End call tool | On | The tutor says goodbye and ends the call itself, so the learner never has to hang up on a silent line. |
| Text normalisation | On | Numbers such as "48 hours" or "5 pm" are read out naturally. |

## Safety

| Setting | Value | Why |
|---|---|---|
| Built-in guardrails | Focus, manipulation (prompt injection) and content | A public link will be tested with off-topic questions and attempts to extract the prompt. Prompt-injection attempts end the conversation. |
| Prompt-level guardrails | In the system prompt | The tutor stays on work English, never claims to be from a company, never promises jobs or salaries, and never repeats personal details such as phone numbers. |
| Authentication | Off | The share link only works for a public agent. The trade-off is that anyone with the link can start a call, so each call is capped at 7 minutes. |

## Widget

| Setting | Value | Why |
|---|---|---|
| Mode | Voice and text | Someone whose microphone is blocked can still type. |
| Language menu | On | The learner picks Hindi or English before the call. |
| Hide audio tags in transcript | On | The tutor marks English practice sentences to be read slowly. Those marks are instructions for the voice, not text for the learner. |
| Terms before the call | On | The learner agrees that the call is recorded and processed before it starts. |
