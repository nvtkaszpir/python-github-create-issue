# About

This small python script allows to create issue in github for given project.
You need to create Github API token to send issues - see [here](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/) how.

Based on https://gist.github.com/JeffPaine/3145490 with tweaks.

Also  because [PyGithub](https://github.com/PyGithub/PyGithub) is sometimes overkill.

# Requrements

Standard python-2.7 and above should be sufficient, using standard packages.

# Usage:

Make file executable and see help:

```bash
chmod +x github_create_issue.py
github_create_issue.py -h
```


# Example

First, export env vars, for example:

```bash
export GITHUB_USER=nvtkaszpir
export GITHUB_PASS=<token>
export REPO_OWNER=nvtkaszpir
export REPO_NAME=vagrant-killingfloorstats
```

Create example issue with title, body and apply two labels:

```bash
./github_create_issue.py --title="Test" --body="Hello And Die" -l bug -l jenkins

```

# Contributing

Feel free to fork and pull a request.
