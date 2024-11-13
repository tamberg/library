# Library
A simple, small scale, low volume "library management system" based on GitHub.

> Work in progress, contact thomas.amberg@fhnw.ch

## Goals
- Keep it simple
- Use GitHub features

## Entities
- Item — a thing to be borrowed by users and lent by admins, respectively (a file in this GitHub repository)
- Topic — to group items (a hierarchical directory, or a file with links to redirect, in this GitHub repository)
- Search — to find items by group or item name (a GitHub search for a full or partial directory or file name)
- Request — to borrow this item for n weeks (a new GitHub issue with the item name, user and timestamp)
- Availability check — to list requests for this item (the list of open GitHub issues filtered by the item name)
- User — who borrows items (a GitHub user with the right to search and read files, open new issues)
- Admin — who lends items (a GitHub user with the right to edit, add new files, label and close issues)
- Tag — for `ready`, `out`, `due`, `late` or `closed` requests (by labeling or closing a GitHub issue)

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

### Respond to a request
- Tag request issue with `ready` once available.
- Use issue comments to reach out if necesssary.

### Hand-out an item
- Tag request issue with `out`.

### Recall a due item
- Tag request issue with `due`.

### Remind a late user
- Tag request issue with `late`.

### Remind an overdue user
- Tag request issue with `overdue`.

### Add an item
- Add an item file to a topic directory.
- Add the item to redirecting entries.
- Create check/borrow links by hand.

### Automation
- CLI python script to create links?
- GitHub actions and badges?
- Use issue [template](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)?
