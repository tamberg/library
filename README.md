# Library
A simple, small scale "library management system" based on GitHub.

> Work in progress, contact thomas.amberg@fhnw.ch

## Goals
- Keep it simple
- Use GitHub features

## Entities
- topic: groups items (directory in repository)
- item: is borrowed/lent by user/admin (file in repository)
- request: borrow this item for n weeks (issue with item name, user, timestamp)
- user: borrows items (GitHub user with right to read, open an issue)
- admin: lends items (GitHub user with right to edit, change an issue)

## Use cases
### Find an item
- Use GitHub file search to find an item file in the repository.

### Check availability
- Filter issues for `is:issue is:open "item name", like [this](TODO).

### Request an item
- File a [pre-populated](https://stackoverflow.com/questions/34146618/pre-populate-the-github-new-issue-form-using-the-querystring) issue, like [this](TODO).

### List my requests
- Filter issues for `is:open is:issue author:@me`, like [this](TODO).

### List any user's requests
- Filter issues for `is:open is:issue author:user`, like [this](TODO).

### Respond to a request (admin)
- Tag request issue with `ready` once available.
- Use issue comments to reach out if necesssary.

### Hand-out an item (admin)
- Tag request issue with `out`.

### Recall a due item (admin)
- Tag request issue with `due`.

### Remind a late user (admin)
- Tag request issue with `late`.

### Remind an overdue user (admin)
- Tag request issue with `overdue`.

### Add an item (admin)
- Add an item file to a topic directory.
- Add the item to redirecting entries.
- Create check/borrow links by hand.

### Automation
- CLI python script to create links?
- GitHub actions and badges?
- Use issue [template](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)?
