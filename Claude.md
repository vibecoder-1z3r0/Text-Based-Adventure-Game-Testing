# Inform 7 Game Development & Testing

## Project Overview
This project develops a text-based adventure game using Inform 7, with a focus on automated testing and quality assurance.

## Development Approach

### 1. Game Design
- Define game world (rooms, objects, NPCs)
- Design puzzles and interactions
- Create narrative elements and descriptions
- Plan win/lose conditions

### 2. Testing Strategy

#### a) Built-in Test Commands
We'll use Inform 7's `Test` command feature to create automated test sequences:
```inform7
Test puzzle-solution with "take key / unlock door / open door"
Test bad-path with "go north / go south / take invalid-object"
```

#### b) Test Coverage Areas
- **Navigation**: Verify all rooms are accessible
- **Puzzle Logic**: Test correct and incorrect solutions
- **Object Interactions**: Ensure objects behave as expected
- **Edge Cases**: Test unusual command sequences
- **Win/Lose Conditions**: Verify game endings work
- **Invalid Commands**: Handle errors gracefully

#### c) Regression Testing
- Maintain a suite of test commands
- Run tests after each significant change
- Document expected outcomes

### 3. Development Workflow

```
1. Design → Write game section
2. Implement → Code in Inform 7
3. Test → Create test commands
4. Compile → Build game
5. Verify → Run tests
6. Iterate → Fix issues and repeat
```

### 4. Project Structure

```
/
├── game/               # Main game source
│   └── story.ni       # Inform 7 source file
├── tests/             # Test scripts
│   └── test-suite.txt # Command sequences
├── builds/            # Compiled games
├── docs/              # Documentation
└── Claude.md          # This file
```

### 5. Quality Assurance

- **Syntax Checking**: Inform 7 compiler feedback
- **Logic Testing**: Test commands for game mechanics
- **Playthrough Testing**: Manual full game walkthroughs
- **Edge Case Testing**: Unusual player behaviors
- **Documentation**: Comment complex rules and mechanics

## Inform 7 Examples

### Basic Room and Object Definitions

```inform7
"Simple Game" by Author

The Kitchen is a room. "A cozy kitchen with wooden cabinets and a large table."

The table is in the Kitchen. The table is a supporter.
The description is "A sturdy oak table."

The silver key is on the table. The description is "A small silver key with intricate engravings."
```

### Containers and Supporters

```inform7
The wooden chest is in the Library. The wooden chest is a closed openable container.
The description is "An old chest with brass fittings."

The bookshelf is in the Library. The bookshelf is a supporter.
The ancient tome is on the bookshelf.
```

### Rooms with Connections

```inform7
The Kitchen is a room.
The Living Room is north of the Kitchen.
The Garden is east of the Kitchen.
The Cellar is below the Kitchen.

The cellar door is a door.
The cellar door is below the Kitchen and above the Cellar.
The cellar door is lockable and locked.
The silver key unlocks the cellar door.
```

### Custom Properties and Rules

```inform7
A thing can be magical or mundane. A thing is usually mundane.

The crystal orb is in the Tower. The crystal orb is magical.

Instead of taking a magical thing:
    say "As you touch [the noun], it glows with an eerie light!";
    now the noun is in the player's inventory.
```

### NPCs and Conversation

```inform7
The wizard is a person in the Tower.
The description is "An elderly wizard in flowing blue robes."

Instead of asking the wizard about "spell":
    say "'The spell requires three ingredients,' the wizard explains."

Instead of giving the crystal orb to the wizard:
    say "The wizard takes the orb and nods approvingly.";
    remove the crystal orb from play;
    now the magic scroll is in the player's inventory.
```

### Puzzle Example: Combination Lock

```inform7
The safe is in the Office. The safe is a closed openable container.
The safe can be unlocked-state or locked-state. The safe is locked-state.

The combination is a number that varies. The combination is 0.

Understand "set safe to [number]" as setting it to.
Setting it to is an action applying to one number.

Carry out setting it to:
    now the combination is the number understood;
    if the combination is 7394:
        now the safe is unlocked-state;
        now the safe is open;
        say "Click! The safe opens.";
    otherwise:
        say "Nothing happens."
```

### Win Condition

```inform7
The treasure is in the safe.

After taking the treasure:
    say "You've found the legendary treasure! You win!";
    end the story saying "You have won".
```

### Test Commands

```inform7
Test quick-win with "n / take key / unlock door / open door / d / take treasure"

Test exploration with "look / i / x table / x key / take key / i"

Test puzzle-solving with "x safe / set safe to 1234 / set safe to 7394 / take treasure"

Test npc-interaction with "x wizard / ask wizard about spell / give orb to wizard"

Test bad-commands with "fly / teleport / eat table / go nowhere"
```

### Scenes and Timed Events

```inform7
Chapter - Scenes

The Dark Night is a scene.
The Dark Night begins when play begins.
The Dark Night ends when the player is in the Tower.

When Dark Night begins:
    say "The night is dark and full of mysteries..."

When Dark Night ends:
    say "As you enter the tower, dawn breaks!";
    now the sun is in the Sky.
```

### Custom Actions

```inform7
Understand "ring [something]" as ringing.
Ringing is an action applying to one thing.

Check ringing:
    if the noun is not the bell:
        say "You can't ring that." instead.

Carry out ringing the bell:
    say "DONG! The bell rings loudly."
```

### Complex Puzzle: Multi-Item Combination

```inform7
The ritual is a scene.
The ritual begins when the candle is lit and the tome is on the altar and the player is in the Chamber.

When the ritual begins:
    say "The room fills with mystical energy!";
    now the portal is in the Chamber;
    now the portal is open.

The candle is in the Chamber. The candle can be lit or unlit. The candle is unlit.
The altar is in the Chamber. The altar is a supporter.
The tome is carried by the player.

Understand "light [something]" as lighting.
Lighting is an action applying to one thing.

Carry out lighting the candle:
    now the candle is lit;
    say "The candle flickers to life."
```

## Tools & Environment

- **Language**: Inform 7
- **Compiler**: inform7-cli (command-line)
- **Testing**: Built-in Test commands + scripted walkthroughs
- **Version Control**: Git
- **Platform**: Linux-based development

## Current Status

- [x] Project initialized
- [x] Testing approach defined
- [ ] Game design complete
- [ ] Initial implementation
- [ ] Test suite created
- [ ] First playable version

## Next Steps

1. Design game world and puzzle
2. Implement in Inform 7
3. Create comprehensive test suite
4. Set up build and test automation
5. Iterate and refine

---

*Last Updated: 2025-11-20*
