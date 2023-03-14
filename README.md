# tiny
A command line tool to that makes tinyurl links quick &amp; easy. It uses the Tinyurl API to make the link, and outputs it in Markdown format.

Example:

![tiny-demo](https://user-images.githubusercontent.com/63665667/224925337-2153ca95-a3a9-4d8c-ae5c-1514df3efb8c.gif)

## Installing on Linux or Windows WSL
Make sure you have the Python dependency `requests` installed, it's needed for the API call

```
python3 -m pip install requests
```

Clone this repo

```
git clone https://github.com/martinlillebo/tiny/
```

If you use `Bash` instead of `Zsh` as your daily shell, you must rename `tiny.zsh` to `tiny.sh`

In your shell's runcommand file, add the cloned directory's path to your PYTHONPATH, and also an alias that runs the `tiny` shell script:

```
export PYTHONPATH="${PYTHONPATH}:/your/tiny/script/folder/path/here"
alias tiny='source /your/tiny/script/folder/path/tiny.zsh'
```

And you're done!

## Quick notes
`tiny` is split into two files: A Python script that does the API call, and a Zsh shell script that gets the input values and passes them to the Python script. In retrospect, everything could easily have been a single Python script. But it works, so I haven't bothered refactoring it
