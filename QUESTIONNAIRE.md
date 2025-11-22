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
- **Your answer:** **At least 4 rubber ducks sitting below his monitors. One duck is named "The Dread Pirate Roberts" and has a trimmed-down post-it on the monitor serving as the duck's name placard. He has dual monitors + a laptop for the 3rd monitor setup (but it looks like he's working from 20 monitors due to all the windows/terminals open).**

  **Programming books scattered around:**
  - "Implementing Quantum Entanglement in Java"
  - "The Heap, the Stack, and You"
  - "It's Not DNS, It's Always DNS"
  - "Heap Dumps and Mem Leaks"
  - "Python Isn't Just About Snakes"
  - "YAML in Spaces"
  - "The Designs of Everyday Things"
  - "Assembler: Why Oh Why?"
  - "CP1610 Game Development"
  - "The 3 Ds of Automation"
  - "How to Write Software That No One Will Read"
  - "Insert Token, Push Button, Get Snack - LLMs the Wrong Way"

### Q5: What absurd project are they working on?
- Examples:
  - "Refactoring the blockchain AI neural network"
  - "Contributing to GNU/Hurd rewrite in Rust"
  - "Implementing quantum entanglement in JavaScript"
  - Something else?
- **Your answer:** **Writing bytecode compiler for HTCPCP (Hyper Text Coffee Pot Control Protocol) - the April Fools' RFC 2324. Perfect blend of coffee obsession and obscure internet protocol nerdery. He occasionally mutters and laments about "418 I'm a teapot" status codes while debugging.**

### Q6: Are they wearing headphones?
- If YES: Can they still hear the player talk to them?
- **Your answer:** **Yes, has over-ear headphones (established in Q2). Most of the time they're down around his neck so he CAN hear you. Occasionally he'll put them on for a brief moment, bob his head to the music, then slide them back down around his neck. This is another repetitive behavior to observe.**

### Q7: Any other repetitive behaviors besides trying to drink empty coffee?
- **Your answer:** **Summary of all repetitive behaviors:**
  1. **Empty coffee mug**: Tries to drink from it, looks inside, sighs when empty, sets it down, repeats
  2. **Headphone music moments**: Occasionally puts headphones on for a brief moment and bobs his head to music (you can hear snippets - sounds like chiptune mixed with heavy metal mixed with early 60s pop Beatles and their later 60s experimental stuff), then slides them back down around his neck
  3. **Pushes glasses up**: Periodically adjusts his thick glasses (established in GAME_DESIGN.md)
  4. **Mutters about 418**: Occasionally laments about "418 I'm a teapot" status codes while debugging his HTCPCP compiler

---

## SECTION 2: VENDING MACHINE PUZZLE (Initial/Warmup)

### Q8: What is the player's initial state?
- How does being "too hungry to think/hear" manifest in the game?
- Examples:
  - Can't hear the engineer's sighs/mutterings?
  - Can't focus enough to notice details?
  - Text is fuzzy or confusing?
  - Room descriptions are minimal?
- **Your answer:** **"Tunnel vision" hunger state:**
  - **Can't focus on details**: Most descriptions are minimal/foggy
  - **Room descriptions are sparse**: Only essential elements visible
  - **Can't notice Merl's behaviors**: His repetitive actions (coffee mug, headphones, etc.) aren't visible to you - too distracted
  - **BUT clear focus on survival**: Token, vending machine, and snack are perfectly clear (tunnel vision effect)
  - **Periodic reminder**: "Your stomach growls" message appears every 5-10 turns (randomized) to remind player they're hungry
  - **Only one snack available**: Located at position **C3** in the vending machine
  - **Easter egg**: When snack is dispensed, display shows "PO" briefly - player thinks it means "Purchase Offered" and shrugs it off (actually completes C-3PO reference)

### Q9: Where is the vending machine located?
- Break room? Hallway? Your cubicle area?
- **Your answer:** **Hallway - positioned between Merl's cubicle/work area and the kitchen/break room area. Serves as a transition space between the two main zones.**

### Q10: Where does the player find the token?
- Option A: Already in your pocket/inventory
- Option B: On your desk
- Option C: Need to find it somewhere
- Option D: Other?
- **Your answer:** **Option D - In the vending machine's coin return slot. A forgotten token from a previous transaction.**

### Q11: If player needs to find the token (Q10 = C), where is it?
- **Your answer:** **In the vending machine's coin return slot. Visual hint: The vending machine description mentions something "shiny" visible in the coin return slot, drawing the player's attention. Commands like "examine coin return", "check coin return", or "look in coin return" will reveal and allow taking the token.**

### Q12: What snacks are in the vending machine?
- Just one option or multiple choices?
- What are they? (chips, candy bar, granola bar, energy bar, etc.)
- **Your answer:** **Only one snack: "Byte Bar" - Wrapper says "8 bits of nutrition!" Perfect tech pun for the programmer theme. Located at position C3 (established in Q8).**

### Q13: What happens after player eats the snack?
- What specifically changes?
- Examples:
  - "Your head clears. You can think again."
  - Can now hear engineer's coffee mug attempts?
  - Can now notice more details in room descriptions?
- **Your answer:** **After eating the Byte Bar, three things change:**
  1. **Hunger satisfied / head clears**: "The fog in your mind lifts. You can think clearly again."
  2. **Room descriptions expand**: Rooms go from sparse/minimal to full, detailed descriptions with all objects visible
  3. **Can now notice Merl's repetitive behaviors**: Empty coffee mug attempts, sighing, headphone bobbing, pushing glasses up, muttering about "418 I'm a teapot" - these were always happening but you were too distracted to notice

  **Note**: Merl's speech was ALWAYS understandable (not garbled), you just weren't paying attention before due to hunger tunnel vision.

### Q14: Is the vending machine puzzle required to progress?
- Option A: Yes, must eat before you can notice the coffee puzzle
- Option B: No, it's optional (just helpful)
- **Your answer:** **Option A: Yes, must eat before you can notice the coffee puzzle. The mechanics established in Q13 confirm you cannot observe Merl's repetitive behaviors (especially the empty coffee mug attempts) until AFTER eating the Byte Bar. This makes the vending machine puzzle a required tutorial/warmup that unlocks the main coffee puzzle.**

### Q15: Any funny/absurd text for the vending machine or snacks?
- Vending machine description?
- Snack wrapper description?
- **Your answer:**

  **Token:**
  - Worn metallic token with ambiguous marking that could be read as "10", "01", or "IO" depending on how you look at it (nod to vibecoder 1.z3r0)

  **Vending Machine:**
  - **Display screen**: Says "Insert Token" (when empty/waiting)
  - **Warning labels**: "Do Not Shake" and "Contains Food-Like Substances"
  - **Physical condition**: The glass and frame look like they were once attacked by a rabid wolverine, or a hungry developer - not sure which
  - **Coin return**: Something shiny visible inside (the token)

  **Byte Bar wrapper:**
  - **Manufacturer**: "0g" (pronounced "Zero Gram")
  - **Main text**: "Byte Bar" and "8 bits of nutrition!" (established in Q12)
  - **Ingredient claim**: "Free of Malloc()s and Null Pointers" (parody of health food labels)
  - **Wrapper design**: Everything else on the wrapper is written in 0s and 1s (binary), except the product name, company name, and ingredient claim
  - **Position**: C3 in vending machine (established in Q8)

---

## SECTION 3: COFFEE PUZZLE

### Q16: Coffee machine complexity - how hard is it to brew coffee?
- Option A: Simple - just "brew coffee" and it works
- Option B: Medium - need to find coffee grounds, add water, press button (3 steps)
- Option C: Complex/Absurd - multi-step ridiculous process (clean filter, grind beans, sacrifice to coffee gods, etc.)
- **Your answer:** **Between Option B and C - Multi-step with absurd comedy elements, but not overly complex. The 418 teapot swap is the key comedic moment (callback to Merl's "418 I'm a teapot" lament).**

### Q17: Based on your answer to Q16, what EXACTLY are the steps to brew coffee?
- List the specific actions the player must take:
- **Your answer:**
  1. **Plug in the coffee maker** (it's currently unplugged)
  2. **Remove the pot labeled "418"** from the coffee maker (it's a teapot - callback to Merl's "418 I'm a teapot" lament)
  3. **Insert the pot labeled "C0FF33"** into the coffee maker (the proper coffee pot - hex/leetspeak for COFFEE)
  4. **Find coffee grounds** and add them to the filter
  5. **Brew coffee** (press the button/start brewing)

### Q18: Where are the coffee-making ingredients/items located?
- Coffee grounds: **At the player's desk (visible only after eating the Byte Bar - absurd detail that the solution was right there all along)**
- Water: **Already in the coffee maker reservoir (one less step)**
- Filter (if needed): **Assume filter already in coffee maker (or not needed)**
- Other items:
  - **C0FF33 pot**: On a table in the kitchen area (visible only after eating the Byte Bar)
  - **418 pot**: Already IN the coffee maker at game start (visible when investigating after eating snack)
  - **Power plug**: Right next to the coffee maker (discovered when investigating the coffee maker area)

### Q19: How does the engineer know coffee is ready?
- Option A: Smell automatically triggers them to leave (player doesn't need to do anything)
- Option B: Player needs to tell them "coffee's ready" or similar
- Option C: Player needs to bring them a cup
- Option D: Something else?
- **Your answer:** **Option B with magical absurdity: Player tells Merl the coffee is ready. If coffee IS actually brewed, Merl can smell it in the air. In a wink of his eye and tip of his hat, you swear his ball cap transforms into a pointy floppy wizard hat as he disappears in a flash to get coffee. His chair is left spinning as the magical vibes dissipate. (Pays off the "open source wizard" theme with literal wizard transformation!)**

### Q20: What happens when engineer leaves for coffee?
- Option A: They stay in the break room permanently (no time pressure)
- Option B: They return after X turns (creates urgency)
- Option C: Something else?
- **Your answer:** _______________

### Q21: If they return (Q20 = B), how many turns before they come back?
- **Your answer:** _______________

---

## SECTION 4: ROOM LAYOUT & NAVIGATION

### Q22: How many rooms total in the game?
- Option A: Minimal (2-3 rooms)
- Option B: Medium (4-5 rooms)
- Option C: Larger (6+ rooms)
- **Your answer:** _______________

### Q23: What specific rooms exist in the game?
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

### Q24: Where does the player start the game?
- **Your answer:** _______________

### Q25: Draw the room connections (which rooms connect to which)?
Example format: "Your Cubicle is west of Hallway. Break Room is east of Hallway."
- **Your answer:**
_______________
_______________
_______________
_______________

---

## SECTION 5: KEYBOARD & POST-IT

### Q26: What happens if player tries to take/lift keyboard while engineer is there?
- What's the funny/absurd rejection message?
- **Your answer:** _______________

### Q27: When engineer is gone, what command(s) work to access the post-it?
- Option A: "lift keyboard" only
- Option B: "look under keyboard" only
- Option C: Both A and B work
- Option D: Something else?
- **Your answer:** _______________

### Q28: What exact text is written on the post-it note?
- Examples: "Password: hunter2", "Password: C0ff33IsL1f3", "Password: correct_horse_battery_staple"
- **Your answer:** _______________

### Q29: Is the post-it immediately visible when keyboard is lifted?
- Option A: Yes, immediately visible
- Option B: Need to search or examine more carefully
- **Your answer:** _______________

---

## SECTION 6: NPC INTERACTIONS

### Q30: What does engineer say if you ask them about the password?
- Option A: "Mmph, check under my keyboard" (spoils puzzle)
- Option B: "Can't talk, debugging critical race condition" (doesn't spoil)
- Option C: They ignore you completely
- Option D: Something else?
- **Your answer:** _______________

### Q31: What does engineer say/do if you ask/tell them about coffee?
- **Your answer:** _______________

### Q32: What other topics can you ask the engineer about? (besides LLMs which we have)
List topics and their responses:
- Topic: _______________ → Response: _______________
- Topic: _______________ → Response: _______________
- Topic: _______________ → Response: _______________

---

## SECTION 7: WIN CONDITION

### Q33: What triggers victory?
- Option A: Just reading the post-it = instant win
- Option B: Taking the post-it = instant win
- Option C: Need to actually use the password to log into your computer
- Option D: Something else?
- **Your answer:** _______________

### Q34: What is the exact victory message?
- **Your answer:** _______________

---

## SECTION 8: FAILED ATTEMPTS & COMEDY

### Q35: What happens if you try to push/move the engineer physically?
- **Your answer:** _______________

### Q36: What happens if you try to unplug their computer/monitors?
- **Your answer:** _______________

### Q37: What happens if you try to take their coffee mug?
- **Your answer:** _______________

### Q38: What happens if you try to talk to them when they're in "the zone"?
- **Your answer:** _______________

### Q39: Any other funny failed attempts you want custom responses for?
- Attempt: _______________ → Response: _______________
- Attempt: _______________ → Response: _______________

---

## SECTION 9: OBJECTS & DETAILS

### Q40: What's at YOUR desk (the player's workstation)?
- Locked computer? Personal items? Your own coffee mug? Stress ball?
- **Your answer:** _______________

### Q41: What's in the break room besides the coffee maker?
- Refrigerator? Microwave? Vending machine? Sink? Table and chairs?
- **Your answer:** _______________

### Q42: Are there any red herrings (objects that seem useful but aren't)?
- **Your answer:** _______________

---

## SECTION 10: OPTIONAL FEATURES

### Q43: Should there be a turn limit or time pressure?
- **Your answer:** _______________

### Q44: Should there be alternate ways to solve the puzzle?
- If yes, describe: _______________

### Q45: Any easter eggs or hidden jokes you want to include?
- **Your answer:** _______________

### Q46: Any other NPCs in the office?
- Manager? Intern? Janitor? Coworkers?
- **Your answer:** _______________

---

## SECTION 11: TONE & FLAVOR

### Q47: Tone for room descriptions - dry/deadpan, over-the-top, or mix?
- **Your answer:** _______________

### Q48: Any other running gags besides the coffee mug attempts?
- **Your answer:** _______________

### Q49: Any other absurd visual details like the "3 monitors look like 7" effect?
- **Your answer:** _______________

---

*We'll go through these ONE AT A TIME. Ready to start with Q1?*
