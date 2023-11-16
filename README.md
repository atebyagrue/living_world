# living_world
An Evennia-based MUD with minimalist game systems to act as a stepping stone for creating your own custom MUD game.

NOTE: please see [our wiki](https://github.com/atebyagrue/living_world/wiki) for any additional details or steps.

## Summary
The intent of this doc is to focus on the codebase & how to set it up & use it. For background on the game itself, please consult the wiki.

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
        pip install evennia pre-commit pywin32pip
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
