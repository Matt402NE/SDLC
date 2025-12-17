# Best Practices for the Syntax of Commit Message

This guide is an outline of the best practices for your Git commit message.  You should have already [created a new branch](Branch%20Creation.md) and made your changes.  Now that you are ready to commit your changes — you need to define your `<commit-message>` that you will use to [commit your changes](Branch%20Commit.md).

Git commits are a way to record changes to a repository and the "message" is a way for you to communicate to other developers that will review your changes in the future.

## Git Commit Message Structure

There are two main components of a Git commit message: the title or summary, and the description. The message title should be limited to 50 characters and the description should be limited to 50 characters.  This means the overall commit message should be less than 120 characters in total. You want to create a message that is detailed enough to be easy to understand and brief enough to be easy to read.

### 1. Message Format Conventions

Messages should be made up of 3 separate sections. 

``` markdown
"{type}({scope}): {description}"
```

| **Argument**    | **Description**                                                                                  |
| --------------- | ------------------------------------------------------------------------------------------------ |
| `{type}`        | Message Type —  standard values indicating the type of commit.                                   |
| `{scope}`       | Message Scope — ticket number should be used to provide additional context about the changes.    |
| `{description}` | Message Description — short description that describes why the code changes are being committed. |

### Section 1: Message Type Rules

The type rule should follow the same type rules defined in [our branch naming convention](Branch%20Naming%20Conventions.md).


### Section 2: Message Scope Rules

The scope provides context about what part of the codebase or which ticket is affected. If your commit affects multiple tickets, choose the primary ticket for the scope. You can reference additional tickets in the commit body if needed.

**When to include scope:**
- **Required**: When your work is tied to a ticket
- **Optional**: For minor changes without tickets (use `no-ref` or omit)
##### Additional Formatting

- **Lowercase**: All alphabetic characters should be lowercase.


### Section 3: Description Rules

The `{description}` should contain a concise description of the change.

- The description is a **mandatory** part
- Use the imperative, present tense: "change" not "changed" nor "changes"
    - Think of `This commit will...` or `This commit should...`
- **Do not** capitalize the first letter
- **Do not** end the description with a period (`.`)


## Examples

### Good Commit Messages ✓

- `feat(t-456): add user authentication system`
- `feat(issue-789): implement password reset functionality`
- `feat(t-234): add two-factor authentication`
- `docs: update api endpoint documentation`
- `fix: resolve critical payment processing bug`

### Bad Commit Messages ✗

- `add login feature` ❌ (no type, no scope)
- `fix bug` ❌ (no scope, too vague)
- `update code` ❌ (no type, no scope, not descriptive)
- `feat: new stuff` ❌ (no scope, vague description)
- `fix(t-456): fix` ❌ (too vague, doesn't explain what was fixed)


