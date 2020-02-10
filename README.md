# Gitfluence

> Confluence to git converter

## Installation

sudo apt install pandoc python3-pygit2 python3-requests

## API Token

https://confluence.atlassian.com/cloud/api-tokens-938839638.html

## Limitations

- Confluence doesn't track renames, so only the current location of a page is
  used. If a page was moved between two runs, it is moved in git once the
  parent page exists.
- Publishing a page in Confluence creates a new version, even if there are no
  changes. This results in an empty commit on the git side.
- Attachments, labels, button states (action items) and collaborators are
  currently not saved. This could result in empty commits.
