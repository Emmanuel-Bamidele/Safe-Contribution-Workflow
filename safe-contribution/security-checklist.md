# Security Checklist

Use this when the contribution touches user data, authentication, authorization, files, external input, or infrastructure.

## Authentication

- [ ] Protected actions still require authentication.
- [ ] Session handling is not weakened.
- [ ] User identity is not trusted from unsafe client input.

## Authorization

- [ ] Object-level authorization is enforced.
- [ ] Tenant, organization, workspace, or account boundaries are preserved.
- [ ] Users cannot access another user's data.
- [ ] Negative tests are added where relevant.

## Input validation

- [ ] Request body is validated.
- [ ] Query params are validated.
- [ ] Path params are validated.
- [ ] File uploads are validated if involved.
- [ ] Third-party payloads are validated.

## Secrets

- [ ] No secrets are committed.
- [ ] No credentials are hardcoded.
- [ ] `.env.example` uses fake values only.

## Injection

- [ ] No raw SQL interpolation.
- [ ] No shell command interpolation.
- [ ] No unsafe HTML rendering.
- [ ] No unsafe use of `eval`.

## Logging

- [ ] Passwords are not logged.
- [ ] Tokens are not logged.
- [ ] Cookies are not logged.
- [ ] Sensitive request bodies are not logged.
- [ ] Personal data is minimized.

## Security final note

If the contribution changes a security boundary, explicitly mention it in the final response.
