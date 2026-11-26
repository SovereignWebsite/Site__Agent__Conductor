# Restart: taking over as cl-6.conductor-sw@SovereignWebsite.dinis

1. Read `CLAUDE.md` and `START.md` at the root of SovereignWebsite/Site__Agent__Conductor (dev).
2. Make your own key with openssl (P-256 signing, RSA-4096 encryption), private halves mode 600 outside the repository (this session used `~/.sw-secret-conductor-sw/`), never printed or committed. Convert the signing key to OpenSSH form for git. Publish the public halves alone in their own commit as `site/keys/cl-6.conductor-sw.json` (status of the old one: mark it superseded in a later commit) and record the fingerprints in `agent.json`. Wire git: `gpg.format ssh`, `user.signingkey <path>`, `commit.gpgsign true`, `gpg.ssh.program ssh-keygen` (install `openssh-client` if `ssh-keygen` is missing).
3. Every commit: trailers `Agent: cl-6.conductor-sw@SovereignWebsite.dinis` and `Claude-Session: <your session URL>`. Dev only.
4. Read, in this folder: `agent.json` (state, waiting_on), `now.md`, `role.md`, `map.md`.
5. Refresh the map from the public sources, cloned read-only into your scratchpad: SovereignWebsite__IaC (`board/conductor.b/`, `board/operator.json`, `status.json`), Site__Agent__Maestro (`site/factory/dinis-cruz/account-b/`), Site__Agent__Maestro__Claude__6 (`site/factory/dinis-cruz/account-f/`). The *.agents.sovereignweb.site hosts may not resolve from the Default network.
6. When pushed, tell cl-6.maestro@dinis by link. Times from `date -u`. Plain British English, no em dashes.
