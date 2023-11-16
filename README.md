# living_world
An Evennia-based MUD with minimalist game systems to act as a stepping stone for creating your own custom MUD game.

NOTE: please see [our wiki](https://github.com/atebyagrue/living_world/wiki) for any additional details or steps.



## Lexicon / Terms
- Actors: these are the "people" in the game. May be called "Mobs" or "Mobiles" in other games. They typically are interacted with by players & can move around & do stuff.
  - NPCs: are system-controlled actors with rudimentary A.I. to control them & perform actions. NPCs are assigned random personality traits on creation that drive their actions in the world.
  - Players: humans playing the game.
  - Builders: players with elevated privileges that are allowed to add content to the game.
  - Superuser: the creator or the game with max privlieges.
- Room: an in-game "place" where things happen. These may or may not be a room, byut in staad is an abstraction of a location where events can occur. For example, a room might be "A Gas Station Bathroom", but it might also be "A Quiet Beach", or "The Bottom of a Chasm". There is no hard & fast rules for sizing and it is dependedant on the builders' needs. In general, I tend to try to think of a room as a 20'x20' area, but there could be a room that is, "The Edge of a Vast & Uncrossable Ocean", etc.
- Item: an in-game object. Ultimately, they are anything that have individual descriptions when looked at, that is not an Actor or Room. Some may or may not be able to be picked up, or "takable" by players. Items generally have some kind of function, a weight, and a value.

## Current Features (Migrateed TODO Items)
- Transportation
- Retainers
  - NPCs that can be hired by players.
- Rooms
  - Flags
    - Dark: nothing in the room is visible to actors, unless they have true/darksight, are a superuser, or
    - Skill (skill:dv): these rooms require passing a skill check in order to enter; think climbing:10 for a room someone must be able to climb into
      - if a skill chekc fails, the player is not allowed entry. You, however, could implemnt drowning in a "swimming" room, falling in a "climbing" room, etc.
- NPCs
  - Types
  - A.I.
- Items
  - base attributes
  - Types
    - Food
    - Drink
    - Clothing
    - Drugs
    - Containers
    - Clothing
    - Armor
    - Weapons
- Players
  - Homeostasis
  - Disposition
  - Buff/Debuffs
- Misc
  - Grouping
  - Camping
  - Crafting
  - Morale

## TODO

## Setup
### Requirements
- Python 3.x (I used [Chocolatey](https://chocolatey.org/) for Windows package management)
  - python -c "import os, sys; print(os.path.dirname(sys.executable))"
  - C:\ProgramData\chocolatey\bin\python3.11.exe
- Visual Studio Code as an IDE, so you may need to change somethings to work with your specific use-case

### Local Dev Environment
- replace windows line endings with Linux/OSX/BSD ones
    - ```
        git config --global core.autocrlf true
        ```
- setup virtualenv
    - ```
        Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted
        & 'C:\Python311\python.exe' -m venv venv
        .\venv\Scripts\activate
        python -m pip install --upgrade pip
        pip install evennia pre-commit pywin32
        windows users once: py -m evennia

        cd mygame
        evennia migrate
        evennia start
        ```

### Docker Dev Environment
TODO

### Misc
- spaces, 2 per tab
  - I do this to maintain continuity with yaml file formatting
  - also a habit from back in my C coding days, everything had better readability with 2 tabs
- pre-commit hooks
  - auto-formatting Python with [Black](https://black.readthedocs.io/en/stable/index.html)
  - prettifying Markdown with ???

## Use
1. activate virtualenv
2. evennia start
3. code
4. debugging is a bit tricky
   1. attach to process
   2. search for "evennia" (no quotes)
   3. always the second process in the list
   4. if you need to restart to test code changes, it'll sometimes hang; so you may need to evennia reload in the terminal or force quit everything & completely restart evennia
5. go forth & codfiy!

## Troubleshooting
- Error #1
  - Cause: you messed up
  - Fix: do stuff
  - Ref: https://stackoverflow.com/
- Error #2
  - Cause: you messed up
  - Fix: do stuff
  - Ref: https://stackoverflow.com/

## References
- [Our Wiki](https://github.com/atebyagrue/living_world/wiki)
- [Markdown Cheatsheet](https://www.markdownguide.org/basic-syntax/)
- [Evennia](https://github.com/evennia/evennia)
- [GitHub Workflows](https://docs.github.com/en/actions/using-workflows)
- [GitHub CI/CD](https://resources.github.com/ci-cd/)
- [Pre-commit Hooks](https://pre-commit.com/)
