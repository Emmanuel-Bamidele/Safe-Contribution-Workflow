# Current Contribution: Bug Fix Example

## Goal

Fix the bug where users can submit the profile form twice by double-clicking the save button.

## Why this contribution is needed

Double submission can create duplicate update requests and confusing UI behavior.

## Scope

### Allowed changes

- Profile settings form
- Save button pending state
- Related profile form tests

### Not allowed

- Do not redesign the profile page.
- Do not refactor unrelated settings components.
- Do not change authentication behavior.
- Do not modify unrelated form components.

## Required behavior

- Save button is disabled while save is in progress.
- Double-clicking does not send duplicate requests.
- User receives the same success/error feedback as before.

## Existing behavior to preserve

- Existing profile fields remain unchanged.
- Existing validation behavior remains unchanged.
- Existing API endpoint remains unchanged.

## Required tests

- Save button disables during submit.
- Double-click only triggers one submit.
- Error state still displays on failed request.

## Checks to run

```bash
npm test
npm run lint
```

## Risks to consider

- Do not prevent users from retrying after a failed save.
