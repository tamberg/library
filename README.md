# Library
A simple, small scale, low volume "library management system" based on GitHub.

> Work in progress, contact thomas.amberg@fhnw.ch

## Goals
- Keep it simple
- Use GitHub features

## Entities
<details>
<summary>Entities like items, topics, requests, etc. can be mapped to GitHub features.</summary>

### Item
- A thing to be borrowed by users and lent by admins, respectively — a file in this GitHub repository.

### Topic
- To group items — a hierarchical directory, or a file with links to redirect, in this GitHub repository.

### Search
- To find items by group or item name — a GitHub search for a full or partial directory or file name.

### Request
- To borrow this item for _n_ weeks — a new GitHub issue with the item name, user and timestamp.

### Availability
- To list open requests for this item — the list of open GitHub issues filtered by the item name.

### User
- Who borrows items — a GitHub user with the right to search and read files, open new issues.

### Admin
- Who lends items — a GitHub user with the right to edit, add new files, label and close issues.

### Tag
- For `ready`, `out`, `due`, `late` or `closed` requests — by labeling or closing a GitHub issue.
</details>

## Use cases
### Find an item
- Use the GitHub (file) search, to find [an item](Hardware/Microcontrollers/Adafruit_Feather_M4_Express.md).

### Check availability
- Find an item (file) to [check its availability](../../issues?q=is%3Aissue+is%3Aopen+%22Adafruit+Feather+M4+Express%22).

### Request an item
- Find an item (file) to [borrow it](../../issues/new?title=Borrow%20request%20for%20Adafruit%20Feather%20M4%20Express&body=1%20piece%20of%20[this](../blob/main/Hardware/Microcontrollers/Adafruit_Feather_M4_Express.md)%20for%20~2%20weeks.) (new issue).

### List my requests
- Log in to [see your requests]() (issues).

### List any user's requests
- See any [user's requests]() (issues).

### Respond to a request
- Tag a request with `ready`, once the item is available.
- Add comments to a request, reach out, if necesssary.

### Hand-out an item
- Tag request issue with `out`.

### Recall a due item
- Tag request issue with `due`.

### Remind a late user
- Tag request issue with `late`.

### Add an item
- Add an item (file) to a topic (directory).
- Add the item to redirecting entries (files).
- Create [pre-populated links](https://stackoverflow.com/questions/34146618/pre-populate-the-github-new-issue-form-using-the-querystring) to check/borrow.

### Automation
- CLI python script to create links?
- GitHub actions and badges?
- Use an issue [template](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)?
