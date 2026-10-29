# Decisions

Each entry gives the decision, the options considered, and why.

## D1. Teach job words, not general vocabulary

**Options:** general English vocabulary; words for the learner's target job (chosen).

**Why:** an interview for a telecalling or retail job tests the English that job uses. A short, specific list also lets a 5-minute session finish something useful.

## D2. Four role families, 12 words each

**Options:** one role; four role families (chosen); every job type.

**Why:** a role made the list only if it is high-volume for entry-level job seekers and its listings ask for English. Telecalling, sales and retail, back office, and front office pass both tests. Delivery was left out: in a sample of listings, 33 of 38 delivery jobs said no English was required. Twelve words per family gives enough variety across sessions while keeping the whole list inside the prompt, where the tutor can always see it.

## D3. Voice, not flashcards

**Options:** flashcards or a quiz; a voice tutor (chosen).

**Why:** recognising a word on a screen is easier than producing it while speaking. An interview tests producing it.

## D4. Explain in Hindi, practise in English, with English mode as the alternative

**Options:** English only; Hindi only; Hindi explanations with English practice (chosen), with English throughout as a second mode.

**Why:** a learner has to understand the lesson before they can learn from it, and their own language lowers the fear of speaking. The practice stays fully in English. An early version switched its instructions to English part-way through and became harder to follow, so instructions now stay in Hindi from greeting to goodbye.

**Platform constraint:** the language is chosen before the call and stays fixed, so the tutor's mode is set by the first message it says. Automatic language detection is off, because a learner speaking an English practice sentence could otherwise switch the whole call to English.

## D5. Five words in about five minutes

**Options:** a longer lesson; 5 words in about 5 minutes (chosen).

**Why:** the learner practises in short breaks on a phone. A hard 7-minute cap leaves room for a slow learner. A learner who asks the tutor to slow down gets 4 words instead of 5, so the session still reaches the recap and the goodbye.

## D6. A three-step ladder for each word

**Options:** ask for an original sentence straight away (versions 1 to 3); a ladder of repeat, change one part, own sentence (chosen).

**Why:** testing showed that making a sentence on demand was where a nervous speaker stalled. Words that needed corrections took 50 to 80 seconds, against 29 seconds when right first time. The ladder builds confidence first. The own-sentence step comes only when the first two steps were right without help, and it always offers a starter.

**Adaptations:**
- a learner who struggles on two words, or can't make their own sentence twice, stays on the first two steps;
- a learner who gets the first two words right first time starts later words at "change one part";
- "I don't know" at the own-sentence step gets a sentence to repeat, never pressure.

**Trade-off:** a struggling learner may not reach the own-sentence step in a session.

## D7. Check the whole sentence; two tries per step

**Options:** check only the target word; check the whole sentence (chosen). For retries: unlimited; one retry per word; two tries per step and at most four per word (chosen).

**Why:** a recruiter notices a missing *a* or *the* as much as a wrong word. Corrections show the right sentence and name the change in a few words, never a grammar lecture. Real mistakes are corrected; a sentence that is correct but could be more natural is accepted, with the natural phrase mentioned once. The try limit protects both the learner's confidence and the session length.

## D8. A spoken recap that ends at the missing word

**Options:** a written fill-in-the-blank; a spoken sentence that stops just before the word, with a Hindi clue (chosen).

**Why:** in a voice call, a gap in the middle of a sentence is hard to follow, and an early version read out the word "blank". The recap now uses only words taught in that session, gives the word's Hindi meaning as a clue, and stops right before the word, so there is one clear answer.

## D9. Word lists inside the prompt

**Options:** a searchable knowledge base; the list inside the prompt (chosen).

**Why:** at 48 words, the tutor can see every word at all times. A search could miss a word or return the wrong one.

## D10. Honest about what it can't do

**Decision:** the prompt tells the tutor it only receives a transcript, so it never praises pronunciation or clarity. It praises what the learner said instead.

**Why:** an early version said "you spoke very clearly" and "good pronunciation", which it could not know, and missed a learner stumbling over a word. False praise teaches the wrong thing and erodes trust.

## D11. A public link with limits

**Options:** a password-protected page; a public link (chosen).

**Why:** a public link is the lowest-friction way for someone to try the tutor. The risks are handled with built-in guardrails, prompt-level rules and a 7-minute cap on every call.
