# Public Repository Boundary

This repository is a **sanitized showcase** for the JoPilot product and architecture. It is **not** the production source repository.

## Intentionally excluded

Do not commit private messages or message databases; names, phone numbers, email addresses, or private relationship data; production databases or backups; credentials, tokens, cookies, or secrets; private configuration; production logs containing personal evidence; fixtures copied from private data; private workspace identifiers; revealing local paths; or production JoPilot source code that has not completed public-release review.

## Public-release rule

Before any production component is copied here, review it for:

1. secrets and credentials;
2. personally identifiable information;
3. private source evidence;
4. embedded IDs and local paths;
5. historical Git content;
6. licensing and dependency implications; and
7. whether the implementation itself should remain private.

When in doubt, document the architecture publicly and keep the implementation private.
