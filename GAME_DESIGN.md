# Game Design Document
## "The Password Hunt" - Office Adventure

### Design Philosophy
**Tone**: Absurd/Comedic (Maniac Mansion / Day of the Tentacle style)
**Core Mechanic**: Environmental puzzle solving with NPC manipulation

---

## Core Concept

**Premise**: You need to log into your computer but forgot the password. Your lead software engineer has it written on a post-it note under their keyboard. Problem: They won't leave their desk.

**Solution**: The engineer is addicted to coffee. Their mug is empty. The cafeteria is out of coffee. You must brew fresh coffee to lure them away from their desk.

---

## What We've Decided So Far

### Confirmed Design Elements:
- **Tone**: Absurd/comedic (Maniac Mansion / Day of the Tentacle style)
- **Main Character**: "Open Source Wizard" lead engineer
  - Typing so fast their hands are a blur
  - 3 physical monitors but looks like 7+ windows open
  - Repeatedly tries to drink from empty coffee mug and sighs
  - Coffee addict (this is the main hint)
- **Core Puzzle**: Brew coffee → Engineer leaves desk → Lift keyboard → Find post-it → Get password
- **Key Constraint**: Cafeteria coffee is out (must brew fresh)
- **Keyboard Mechanic**:
  - Can examine while engineer is there, but it's a blur from rapid typing
  - Cannot lift/access while engineer is present
  - Post-it is hidden underneath

### Still Need to Decide:
- Engineer's name and specific appearance
- What absurd project they're working on
- Coffee brewing complexity (simple vs multi-step puzzle)
- Room layout and navigation
- Exact text on post-it note
- How engineer knows coffee is ready
- Does engineer return (time pressure) or stay away?
- NPC interaction details
- Failed attempt responses (comedy opportunities)
- Win condition details

---

## Design Questions to Answer

### 1. Engineer Character Design

**Name:**
- [ ] Decision needed: What's the lead engineer's name?
  - Options: Dave, Bernard, Steve, something absurd?
  - Your choice: _______________

**Character Archetype:**
- [x] **"Open Source Wizard"** - impossibly fast coder, completely absorbed in their work

**Physical Appearance:**
- [ ] What do they look like?
  - Thick glasses? Hoodie? Band t-shirt?
  - Mechanical keyboard with RGB lights?
  - Your description: _______________

**Desk Environment:**
- [x] **Multiple monitors (3 physical, appears like 7+ with all windows)**
  - Despite having only three physical monitors, the sheer number of terminal windows and IDEs open makes it look like there are at least seven displays
- [x] **Coffee mug** - their favorite mug, always within reach, currently empty
- [ ] What else surrounds them?
  - Empty coffee cups? Pizza boxes? Rubber ducks? Energy drink cans?
  - Stack of programming books? Action figures?
  - Your additions: _______________

**Coding Activity:**
- [ ] What absurd project are they working on?
  - "Refactoring the blockchain AI neural network"?
  - "Contributing to GNU/Hurd"?
  - "Implementing quantum entanglement in JavaScript"?
  - Your choice: _______________

**Behavior Patterns:**
- [x] **Hands are a blur when typing** - fingers move so fast you can't see individual keystrokes, like a typing wizard
- [x] **Periodically tries to drink from empty mug** - lifts mug to lips, looks inside, sighs deeply when realizing it's empty, sets it back down, repeats
- [x] **Coffee addiction** - this is the key hint that coffee is important
- [ ] Wearing headphones? (if yes, can they hear you?)
- [ ] Any other repetitive behaviors? _______________

---

### 2. Coffee Puzzle Mechanics

**Coffee Supply Status:**
- [x] **Cafeteria coffee is out** - this forces the player to actually brew fresh coffee rather than just getting some

**Coffee Machine Complexity:**
- [ ] Simple: Just "brew coffee" command and it works
- [ ] Medium: Need coffee grounds + water + press button
- [ ] Complex/Absurd: Multi-step ridiculous process (clean filter, grind beans, align with stars, etc.)
- Your choice: _______________

**Coffee Ingredients:**
- [ ] What's needed to make coffee?
  - Just press button?
  - Find: grounds, water, filter, mug?
  - Your list: _______________

**Coffee Machine Location:**
- [ ] Where is it located?
  - Break room? Kitchenette? Conference room?
  - Your choice: _______________

**Triggering Engineer Movement:**
- [ ] How does the engineer know coffee is ready?
  - Automatic: Smell triggers them to leave
  - Manual: You tell them "coffee's ready"
  - Physical: You bring them a cup
  - Your choice: _______________

**Engineer's Coffee Behavior:**
- [ ] Do they stay away permanently?
- [ ] Do they return after X turns (creating time pressure)?
- Your choice: _______________

---

### 3. Room Layout & Navigation

**Room Structure (choose one):**
- [ ] Minimal: Your Cubicle (start) ↔ Break Room ↔ Engineer's Cubicle
- [ ] Simple: Just Break Room ↔ Engineer's Cubicle (start here)
- [ ] Medium: Your Cubicle + Hallway + Break Room + Engineer's Cubicle + Conference Room
- [ ] Your custom layout: _______________

**Starting Location:**
- [ ] Player starts in:
  - Your own cubicle?
  - Engineer's cubicle (watching them work)?
  - Hallway?
  - Your choice: _______________

**Additional Rooms (optional):**
- [ ] Bathroom?
- [ ] Server room?
- [ ] Manager's office?
- [ ] Supply closet?
- [ ] Other: _______________

---

### 4. Keyboard & Post-it Mechanics

**The Goal:**
- [x] **Post-it note is hidden under the engineer's keyboard** with the password written on it
- [x] **Cannot access it while engineer is at their desk** - must get them to leave

**Examining Keyboard (while engineer is there):**
- [x] **Can examine but keyboard is a blur from typing** - fingers moving too fast
- [x] **Can't lift/touch it while engineer is using it** - they're actively typing on it
- [x] **Visual effect**: "The keyboard is a blur of motion as [Engineer]'s fingers dance across it at superhuman speed, code appearing on the screens faster than you can read"
- [ ] Additional details for examination? _______________

**Attempting to Take/Move Keyboard:**
- [ ] What happens if player tries to take keyboard while engineer is there?
  - Funny rejection message?
  - Engineer reacts?
  - Your response: _______________

**Looking Under Keyboard (when engineer is gone):**
- [ ] Command to use:
  - "lift keyboard"?
  - "look under keyboard"?
  - Both work?
  - Your choice: _______________

**The Post-it Note:**
- [x] **Contains the password** needed to log into player's computer
- [ ] What's written on it?
  - Simple: "Password: hunter2"
  - Funny: "Password: correct_horse_battery_staple"
  - Absurd: "Password: ILoveCoffee123!"
  - Your text: _______________

**Post-it Visibility:**
- [ ] Is it immediately visible when lifting keyboard?
- [ ] Or need to search/look carefully?
- Your choice: _______________

---

### 5. NPC Interactions

**Talking to Engineer:**
- [x] **Can player talk to them: YES** - they respond but remain absorbed in work
- [x] **Example dialogue provided:**
  > "You know these LLMs? They're just non-deterministic guessing machines..."
  >
  > *The engineer goes back to coding, moving windows around, running a flurry of CLI commands. Things go green and red on the screens. The engineer sighs and tries to drink more coffee.*

**Engineer Personality:**
- [x] Cynical about AI/LLMs
- [x] Very technical, absorbed in work
- [x] Returns to coding immediately after speaking
- [x] Visual activity: windows moving, CLI commands flying, test results flashing green/red

**Asking About Password:**
- [ ] If you ask engineer about password directly:
  - "Mmph, check under my keyboard" (spoils puzzle)
  - "Can't talk, debugging critical race condition"
  - Ignores you completely
  - Your response: _______________

**Asking About Coffee:**
- [ ] If you mention coffee to them:
  - "Mmm, coffee..." (wistful)
  - *tries to drink from empty mug, sighs*
  - Detailed rant about coffee preferences
  - Your response: _______________

**Other Conversation Topics:**
- [x] **LLMs/AI** - confirmed dialogue above
- [ ] What else can you ask/tell them about?
  - Their code/project?
  - Tabs vs spaces?
  - Vim vs Emacs?
  - Programming languages?
  - Your topics: _______________

---

### 6. Win Condition

**Victory Trigger:**
- [ ] Just reading the post-it = instant win?
- [ ] Need to take the post-it?
- [ ] Need to use password to log into your computer?
- [ ] Something else?
- Your choice: _______________

**Win Message:**
- [ ] What's the victory text?
  - Simple: "You got the password! You win!"
  - Descriptive: "You successfully log in and can finally start your workday!"
  - Funny: "With password in hand, you can now check your email and pretend to work!"
  - Your message: _______________

---

### 7. Failed Attempts & Comedy

**Trying to Move Engineer Physically:**
- [ ] What happens if you try to "push engineer" or "move engineer"?
  - Your response: _______________

**Trying to Unplug Computer:**
- [ ] Can you unplug their monitors/computer?
  - What happens?
  - Your response: _______________

**Trying to Take Their Mug:**
- [ ] Can you take the empty mug?
  - What happens?
  - Your response: _______________

**Other Failed Approaches:**
- [ ] What other funny/failed attempts should have custom responses?
  - Your ideas: _______________

---

### 8. Additional Objects & Details

**Engineer's Desk Objects:**
- [ ] What's on/near their desk?
  - Sticky notes? Rubber duck? Action figures? Books?
  - Your list: _______________

**Your Desk (if included):**
- [ ] What's at your workstation?
  - Locked computer? Personal items? Coffee mug?
  - Your list: _______________

**Break Room Objects:**
- [x] Coffee maker (essential)
- [ ] What else?
  - Refrigerator? Microwave? Vending machine?
  - Sink? Table and chairs?
  - Your additions: _______________

**Red Herrings:**
- [ ] Any objects that seem useful but aren't?
  - Ideas: _______________

---

### 9. Humor & Flavor Text

**Absurd Details:**
- [x] Engineer has 3 monitors but looks like 7+ windows
- [ ] What other absurd details?
  - Your additions: _______________

**Running Gags:**
- [x] Engineer repeatedly tries empty mug
- [ ] Other recurring jokes?
  - Your ideas: _______________

**Room Descriptions:**
- [ ] Overall tone for descriptions:
  - Dry/deadpan?
  - Over-the-top?
  - Mix of both?
  - Your preference: _______________

---

### 10. Optional Features

**Time Pressure:**
- [ ] Is there a turn limit?
- [ ] Does something happen if you take too long?
- Your choice: _______________

**Multiple Solutions:**
- [ ] Should there be alternate ways to solve the puzzle?
  - Ideas: _______________

**Easter Eggs:**
- [ ] Any hidden jokes or references?
  - Ideas: _______________

**Additional NPCs:**
- [ ] Anyone else in the office?
  - Manager? Intern? Janitor?
  - Your ideas: _______________

---

## Implementation Checklist

Once design questions are answered:
- [ ] Create game structure
- [ ] Implement rooms and connections
- [ ] Create engineer NPC with behaviors
- [ ] Implement coffee puzzle
- [ ] Add keyboard/post-it mechanic
- [ ] Write flavor text and descriptions
- [ ] Create test suite
- [ ] Test all paths (success, failures, edge cases)
- [ ] Polish and add humor

---

*Last Updated: 2025-11-20*
