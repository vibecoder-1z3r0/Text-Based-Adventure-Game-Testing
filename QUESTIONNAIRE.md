# Game Design Questionnaire
## "The Password Hunt" - Office Adventure

This document contains all design questions we need to answer before implementation.
We'll go through these **ONE AT A TIME** to build the complete game design.

---

## SECTION 1: ENGINEER CHARACTER

### Q1: What is the lead engineer's name?
- Options: Dave, Bernard, Steve, something absurd/funny?
- **Your answer:** **Merl** (short for Merlin, fits the "wizard" theme perfectly)

### Q2: Physical appearance - what do they look like?
- Thick glasses? Hoodie? Band t-shirt? Something else?
- **Your answer:** **Older engineer with a thick Unix-style grey beard, thick glasses, wearing a hoodie and ball cap. Has over-ear headphones. Vibe-coder aesthetic - keeps sunglasses at his desk for when he "vibe-codes"**

### Q3: What's on their mechanical keyboard?
- RGB lights? Vintage mechanical? Custom keycaps? Plain?
- **Your answer:** **Mechanical keyboard similar to the old IBM clicky keyboards (Model M style) but not as obnoxiously loud. Has F-keys down the left side. Meta where Alt could be, or is it Alt where Meta could be? (Classic Unix/Lisp machine confusion). Vintage tactile feel, fits the Unix wizard aesthetic perfectly.**

### Q4: What surrounds their desk besides the monitors and coffee mug?
- Options: Empty coffee cups, pizza boxes, rubber ducks, energy drink cans, programming books, action figures, etc.
- **Your answer:** **At least 4 rubber ducks sitting below his monitors. He has dual monitors + a laptop for the 3rd monitor setup (but it looks like he's working from 20 monitors due to all the windows/terminals open).**

### Q5: What absurd project are they working on?
- Examples:
  - "Refactoring the blockchain AI neural network"
  - "Contributing to GNU/Hurd rewrite in Rust"
  - "Implementing quantum entanglement in JavaScript"
  - Something else?
- **Your answer:** _______________

### Q6: Are they wearing headphones?
- If YES: Can they still hear the player talk to them?
- **Your answer:** _______________

### Q7: Any other repetitive behaviors besides trying to drink empty coffee?
- **Your answer:** _______________

---

## SECTION 2: VENDING MACHINE PUZZLE (Initial/Warmup)

### Q8: What is the player's initial state?
- How does being "too hungry to think/hear" manifest in the game?
- Examples:
  - Can't hear the engineer's sighs/mutterings?
  - Can't focus enough to notice details?
  - Text is fuzzy or confusing?
  - Room descriptions are minimal?
- **Your answer:** _______________

### Q9: Where is the vending machine located?
- Break room? Hallway? Your cubicle area?
- **Your answer:** _______________

### Q10: Where does the player find the token?
- Option A: Already in your pocket/inventory
- Option B: On your desk
- Option C: Need to find it somewhere
- Option D: Other?
- **Your answer:** _______________

### Q11: If player needs to find the token (Q10 = C), where is it?
- **Your answer:** _______________

### Q12: What snacks are in the vending machine?
- Just one option or multiple choices?
- What are they? (chips, candy bar, granola bar, energy bar, etc.)
- **Your answer:** _______________

### Q13: What happens after player eats the snack?
- What specifically changes?
- Examples:
  - "Your head clears. You can think again."
  - Can now hear engineer's coffee mug attempts?
  - Can now notice more details in room descriptions?
- **Your answer:** _______________

### Q14: Is the vending machine puzzle required to progress?
- Option A: Yes, must eat before you can notice the coffee puzzle
- Option B: No, it's optional (just helpful)
- **Your answer:** _______________

### Q15: Any funny/absurd text for the vending machine or snacks?
- Vending machine description?
- Snack wrapper description?
- **Your answer:** _______________

---

## SECTION 3: COFFEE PUZZLE

### Q16: Coffee machine complexity - how hard is it to brew coffee?
- Option A: Simple - just "brew coffee" and it works
- Option B: Medium - need to find coffee grounds, add water, press button (3 steps)
- Option C: Complex/Absurd - multi-step ridiculous process (clean filter, grind beans, sacrifice to coffee gods, etc.)
- **Your answer:** _______________

### Q17: Based on your answer to Q16, what EXACTLY are the steps to brew coffee?
- List the specific actions the player must take:
- **Your answer:**
  1. _______________
  2. _______________
  3. _______________ (if needed)
  4. _______________ (if needed)

### Q18: Where are the coffee-making ingredients/items located?
- Coffee grounds: _______________
- Water: _______________
- Filter (if needed): _______________
- Other: _______________

### Q19: How does the engineer know coffee is ready?
- Option A: Smell automatically triggers them to leave (player doesn't need to do anything)
- Option B: Player needs to tell them "coffee's ready" or similar
- Option C: Player needs to bring them a cup
- Option D: Something else?
- **Your answer:** _______________

### Q12: What happens when engineer leaves for coffee?
- Option A: They stay in the break room permanently (no time pressure)
- Option B: They return after X turns (creates urgency)
- Option C: Something else?
- **Your answer:** _______________

### Q13: If they return (Q12 = B), how many turns before they come back?
- **Your answer:** _______________

---

## SECTION 3: ROOM LAYOUT & NAVIGATION

### Q14: How many rooms total in the game?
- Option A: Minimal (2-3 rooms)
- Option B: Medium (4-5 rooms)
- Option C: Larger (6+ rooms)
- **Your answer:** _______________

### Q15: What specific rooms exist in the game?
Check all that apply and add any custom rooms:
- [ ] Your Cubicle
- [ ] Engineer's Cubicle
- [ ] Hallway
- [ ] Break Room
- [ ] Conference Room
- [ ] Bathroom
- [ ] Server Room
- [ ] Manager's Office
- [ ] Supply Closet
- [ ] Other: _______________
- [ ] Other: _______________

### Q16: Where does the player start the game?
- **Your answer:** _______________

### Q17: Draw the room connections (which rooms connect to which)?
Example format: "Your Cubicle is west of Hallway. Break Room is east of Hallway."
- **Your answer:**
_______________
_______________
_______________
_______________

---

## SECTION 4: KEYBOARD & POST-IT

### Q18: What happens if player tries to take/lift keyboard while engineer is there?
- What's the funny/absurd rejection message?
- **Your answer:** _______________

### Q19: When engineer is gone, what command(s) work to access the post-it?
- Option A: "lift keyboard" only
- Option B: "look under keyboard" only
- Option C: Both A and B work
- Option D: Something else?
- **Your answer:** _______________

### Q20: What exact text is written on the post-it note?
- Examples: "Password: hunter2", "Password: C0ff33IsL1f3", "Password: correct_horse_battery_staple"
- **Your answer:** _______________

### Q21: Is the post-it immediately visible when keyboard is lifted?
- Option A: Yes, immediately visible
- Option B: Need to search or examine more carefully
- **Your answer:** _______________

---

## SECTION 5: NPC INTERACTIONS

### Q22: What does engineer say if you ask them about the password?
- Option A: "Mmph, check under my keyboard" (spoils puzzle)
- Option B: "Can't talk, debugging critical race condition" (doesn't spoil)
- Option C: They ignore you completely
- Option D: Something else?
- **Your answer:** _______________

### Q23: What does engineer say/do if you ask/tell them about coffee?
- **Your answer:** _______________

### Q24: What other topics can you ask the engineer about? (besides LLMs which we have)
List topics and their responses:
- Topic: _______________ → Response: _______________
- Topic: _______________ → Response: _______________
- Topic: _______________ → Response: _______________

---

## SECTION 6: WIN CONDITION

### Q25: What triggers victory?
- Option A: Just reading the post-it = instant win
- Option B: Taking the post-it = instant win
- Option C: Need to actually use the password to log into your computer
- Option D: Something else?
- **Your answer:** _______________

### Q26: What is the exact victory message?
- **Your answer:** _______________

---

## SECTION 7: FAILED ATTEMPTS & COMEDY

### Q27: What happens if you try to push/move the engineer physically?
- **Your answer:** _______________

### Q28: What happens if you try to unplug their computer/monitors?
- **Your answer:** _______________

### Q29: What happens if you try to take their coffee mug?
- **Your answer:** _______________

### Q30: What happens if you try to talk to them when they're in "the zone"?
- **Your answer:** _______________

### Q31: Any other funny failed attempts you want custom responses for?
- Attempt: _______________ → Response: _______________
- Attempt: _______________ → Response: _______________

---

## SECTION 8: OBJECTS & DETAILS

### Q32: What's at YOUR desk (the player's workstation)?
- Locked computer? Personal items? Your own coffee mug? Stress ball?
- **Your answer:** _______________

### Q33: What's in the break room besides the coffee maker?
- Refrigerator? Microwave? Vending machine? Sink? Table and chairs?
- **Your answer:** _______________

### Q34: Are there any red herrings (objects that seem useful but aren't)?
- **Your answer:** _______________

---

## SECTION 9: OPTIONAL FEATURES

### Q35: Should there be a turn limit or time pressure?
- **Your answer:** _______________

### Q36: Should there be alternate ways to solve the puzzle?
- If yes, describe: _______________

### Q37: Any easter eggs or hidden jokes you want to include?
- **Your answer:** _______________

### Q38: Any other NPCs in the office?
- Manager? Intern? Janitor? Coworkers?
- **Your answer:** _______________

---

## SECTION 10: TONE & FLAVOR

### Q39: Tone for room descriptions - dry/deadpan, over-the-top, or mix?
- **Your answer:** _______________

### Q40: Any other running gags besides the coffee mug attempts?
- **Your answer:** _______________

### Q41: Any other absurd visual details like the "3 monitors look like 7" effect?
- **Your answer:** _______________

---

*We'll go through these ONE AT A TIME. Ready to start with Q1?*
