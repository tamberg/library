# Library
A simple, small scale, low volume "library management system" based on GitHub.

> Work in progress, contact thomas.amberg@fhnw.ch

## Goals
- Keep it simple
- Use GitHub features

## Entities
- Item — is borrowed by a user and lent by an admin (a file in this repository)
- Topic — groups items (a directory, or a file with redirect links, in this repository)
- Search — to find items by group or item name (a search for a directory or a file name)
- Request — to borrow this item for n weeks (an issue with the item name, user, timestamp)
- Availability check — to list requests for this item (the list of issues filtered by the item name)
- User — who borrows items (GitHub user with the right to search and read files, open an issue)
- Admin — who lends items (GitHub user with the right to edit, add files to repository, tag an issue)
- Tag — for `ready`, `out`, `due`, `late` requests or `lost` items (a label to tag an issue)

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
