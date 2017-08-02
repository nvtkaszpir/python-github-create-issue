# About

This small python script allows to create issue in GitHub for given project.

Why?

- [PyGithub](https://github.com/PyGithub/PyGithub) is sometimes an overkill
- [Jenkins Github Issues](https://wiki.jenkins.io/display/JENKINS/GitHub+Issues+Plugin) plugin is not fully mature yet (not to mention it's groovy specific)
- other packages - forcing yourself to install ruby or nodejs is .... eh.
- bash - yeah I could make a curl with some input file but integration might be more problematic in certain areas.

Based on https://gist.github.com/JeffPaine/3145490 with tweaks.

# Requrements

Standard python-2.7 provided with any decent Linux distribution should be sufficient, using standard packages.

You need to create GitHub API token to send issues - see [here](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/) how.


# Usage:

Make file executable and see help:

```bash
chmod +x github_create_issue.py
./github_create_issue.py -h
```

# Example

First, export env vars:

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
