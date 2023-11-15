# living_world
An Evennia-based MUD with minimalist game systems to act as a stepping stone for creating your own custom MUD game.

## Setup
### Requirements
- Python 3.x (I used [Chocolatey](https://chocolatey.org/) for Windows package management)
  - python -c "import os, sys; print(os.path.dirname(sys.executable))"
  - C:\ProgramData\chocolatey\bin\python3.11.exe
- stuff

### Local Dev Environment
- replace windows line endings with Linux/OSX/BSD ones
    - ```
        git config --global core.autocrlf true
        ```
- setup virtualenv
    - ```
        Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted
        & 'C:\Python311\python.exe' -m venv venv
        & 'C:\Program Files\Python311\python.exe' -m venv venv

        & 'C:\ProgramData\chocolatey\bin\python3.11.exe' -m venv venv

        .\venv\Scripts\activate
        python -m pip install --upgrade pip
        pip install evennia pre-commit pywin32
        windows users once: py -m evennia

        cd mygame
        evennia migrate
        evennia start
        ```

### Docker Dev Environment
### Misc
- spaces, 2 per tab
- replace window line returns
- pre-commit hooks
- auto-formatting with [Black](https://black.readthedocs.io/en/stable/index.html)

## Use

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
- https://www.markdownguide.org/basic-syntax/
- [Evennia](https://github.com/evennia/evennia)
- https://docs.github.com/en/actions/using-workflows
- https://resources.github.com/ci-cd/
- https://pre-commit.com/
