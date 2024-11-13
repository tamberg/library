# Library
A simple, small scale "library management system" based on GitHub.

> Work in progress, contact thomas.amberg@fhnw.ch.

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
- Use GitHub search to find an item file in the repository.

### Borrow an item
- File a GitHub issue to ask for an item.
- Get items sent to you or fetch it in person.

### Lend an item
- Add a task to the project board using the loan [template](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository).
- Edit the item file to indicate availability, link loan.

### Add an item
- Add an item file to a topic directory.
