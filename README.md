# Library
A simple, small scale "library management system" based on GitHub.

> Work in progress, contact thomas.amberg@fhnw.ch

## Goals
- Keep it simple
- Use GitHub features

## Entities
- topic: groups items (directory in repository)
- item: is borrowed/lent by user/admin (file in repository)
- loan: item i by user u from date d, for n weeks (task in project board)
- user: borrows items (GitHub user with right to read, open an issue)
- admin: lends items (GitHub user with right to edit, add a task)

## Use cases
### Find an item
- Use GitHub file search to find an item file in the repository.

### Check availability
- Filter issues for `is:issue is:open "item name", like [this](TODO).

### Request an item
- File a [pre-populated](https://stackoverflow.com/questions/34146618/pre-populate-the-github-new-issue-form-using-the-querystring) issue, like [this](TODO).

### List own borrow requests
- Filter issues for `is:open` `is:issue` `author:@me`, like [this](TODO).

### List any user's requests
- Filter issues for `is:open` `is:issue` `author:user`, like [this](TODO).

### Respond to a borrow request (admin)
- Tag request issue with `ready` once available.
- Use issue comments to reach out if necesssary.

### Lend an item (admin)
- Add a task to the project board using the loan [template](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository).
- Edit the item file to indicate availability, link loan.

### Recall an item (admin)
- Contact user in last loan through linked borrowing issue.
- Communicate using [tags/labels](https://github.com/tamberg/library/issues/labels) `ready`, `out`, `due`, `late`, `returned`, `lost`.

### Add an item (admin)
- Add an item file to a topic directory.
- Create check/borrow links by hand.

### Automation
- CLI python script to create links?
- GitHub actions and badges?
- Use issue [template](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)?
