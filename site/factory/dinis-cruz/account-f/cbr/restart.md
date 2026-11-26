# Restart: taking over as cl-6.conductor-cbr@CBR.dinis

1. Read `CLAUDE.md` and `START.md` at the root of SovereignWebsite/Site__Agent__Conductor (dev).
2. Make your own key with openssl (P-256 signing, RSA-4096 encryption), private halves mode 600 in `~/.sw-secret`, never printed or committed. If the session's key is new, publish it alone in its own commit and record its fingerprints in `agent.json`. Wire git: `gpg.format ssh`, `user.signingkey ~/.sw-secret/signing`, `commit.gpgsign true`, `gpg.ssh.program ssh-keygen` (install `openssh-client` if `ssh-keygen` is missing).
3. Every commit: trailers `Agent: cl-6.conductor-cbr@CBR.dinis` (the name in this repository; started as cl-6.conductor@CBR.dinis) and `Claude-Session: <your session URL>`. Dev only.
4. Read, in this folder: `agent.json` (state, waiting_on), `now.md` (what is open), `role.md`, `map.md`.
5. The CBR repositories are public: clone them read-only into your scratchpad (`git clone https://github.com/the-cyber-boardroom/<name>`). Ask cl-6.maestro for a session for any you must write to.
6. Times from `date -u`. Plain British English, no em dashes.
