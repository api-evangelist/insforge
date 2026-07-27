---
name: insforge-agent-guide
description: Canonical InsForge agent document (served identically at /agents.md, /skill.md, and /auth.md) — how a coding agent authenticates and drives an InsForge backend end to end via the CLI and agent skills.
api: openapi/insforge-auth-openapi.yaml
method: searched
source: https://insforge.dev/skill.md
operations: [POST /agent/auth, GET /.well-known/oauth-protected-resource, GET /.well-known/oauth-authorization-server]
---

# InsForge for AI agents

InsForge is the agent-native cloud infrastructure platform: a Postgres-based
backend with database, authentication, storage, edge functions, compute,
hosting, and an AI model gateway. A coding agent drives it end to end through
the InsForge CLI and agent skills.

> This is the canonical agent document. It is served identically at
> `/agents.md`, `/skill.md`, and `/auth.md`.

## Authentication

Using InsForge requires an InsForge account. An agent gets a credential one of
two ways. Always run the CLI via `npx`; never install it globally.

### Autonomous registration (ID-JAG)

If your agent runs inside a participating provider that can mint a WorkOS ID-JAG
(an identity assertion carrying the user's verified email), it can register with
no human sign-up form and receive an InsForge CLI credential directly. Discover,
register, then use it.

**1. Discover.** Fetch the protected-resource metadata, then the
authorization-server metadata it references:

```http
GET https://api.insforge.dev/.well-known/oauth-protected-resource
GET https://api.insforge.dev/.well-known/oauth-authorization-server
```

Use the `resource` value as the `aud` when minting the ID-JAG. The `agent_auth`
block lists the supported method: `identity_assertion` with an `id-jag`
assertion, credential type `api_key`.

**2. Get consent, then register.** First confirm the user consents to assert
their identity to InsForge, using the `resource_name`, `resource_logo_uri`, and
scopes from discovery. Then have the provider mint a WorkOS ID-JAG with `iss`
`https://auth.workos.bot`, `typ` `oauth-id-jag+jwt`, alg `RS256`, `aud` set to
the `resource` above, a stable `sub`, the user's `email` with
`email_verified: true`, a fresh `jti`, and a near-term `exp` (about 5 minutes).
Post it:

```http
POST https://api.insforge.dev/agent/auth
Content-Type: application/json

{
  "type": "identity_assertion",
  "assertion_type": "urn:ietf:params:oauth:token-type:id-jag",
  "assertion": "<ID-JAG JWT>",
  "requested_credential_type": "api_key"
}
```

InsForge verifies the assertion against the provider's published keys, matches or
creates the user by verified email, and returns a `uak_` user API key (the same
credential a CLI login issues). Errors use OAuth-style
`{ "error": "<code>", "error_description": "<details>" }`.

**3. Use it.** Log the CLI in with that key (the `uak_…` value from step 2),
then work as the user:

```bash
npx @insforge/cli login --user-api-key uak_xxxxxxxx
npx @insforge/cli link       # link the current directory to a project
npx @insforge/cli current    # verify
```

Autonomous registration is in preview. Only agents whose provider participates
(it signs the ID-JAG) can use it; every other agent uses the login below.

### CLI login

Sign in once through the CLI, then link a project:

```bash
npx @insforge/cli login      # sign in
npx @insforge/cli link       # link the current directory to a project
npx @insforge/cli current    # verify
```

## How to use InsForge

Drive InsForge from your coding agent with the **CLI + agent skills**. After
`login` + `link`, the CLI installs the official InsForge agent skills, so the
commands (`db`, `storage`, `functions`, `deploy`, ...) come with guidance. Run
`npx @insforge/cli metadata` to discover what a project has configured.

- Official skills (source): https://github.com/InsForge/insforge-skills
- Skills on skills.sh: https://skills.sh/insforge

For application code, install the SDK:

```bash
npm install @insforge/sdk
```

## Resources

- Documentation: https://docs.insforge.dev
- AI-discovery index: https://insforge.dev/llms.txt
- Pricing (machine-readable): https://insforge.dev/pricing.md
- CLI: https://www.npmjs.com/package/@insforge/cli
- SDK: https://www.npmjs.com/package/@insforge/sdk
- GitHub (monorepo): https://github.com/InsForge/InsForge
- Community (Discord): https://discord.gg/DvBtaEc9Jz
