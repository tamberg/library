# Library
A simple, small scale, low volume "library management system" based on GitHub.

> Work in progress, contact thomas.amberg@fhnw.ch

## Goals
- Keep it simple
- Use GitHub features

## Entities
- Item — a thing to be borrowed by users and lent by admins, respectively (a file in this repository)
- Topic — groups items (a hierarchical directory path, or a file with redirect links, in this repository)
- Search — to find items by group or item name (a search for a full or partial directory or file name)
- Request — to borrow this item for n weeks (a new issue with the item name, user and timestamp)
- Availability check — to list requests for this item (the list of open issues filtered by the item name)
- User — who borrows items (a GitHub user with rights to search and read files, and open new issues)
- Admin — who lends items (a GitHub user with rights to edit, add files to the repository, tag issues)
- Tag — for `ready`, `out`, `due`, `late`, `lost` or `closed` requests (by labeling or closing an issue)

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
