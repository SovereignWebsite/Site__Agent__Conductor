# Restart: how a new session of cl-6.conductor@sgit.dinis takes over

1. Read `CLAUDE.md` and `START.md` at the root of SovereignWebsite/Site__Agent__Conductor.
2. Make your own key (openssl: P-256 signing, RSA-4096 encryption; private halves mode 600 outside the repository) and wire git to sign (`gpg.format ssh`, `gpg.ssh.program ssh-keygen`, `user.signingkey`). A new session's key replaces the old one: mark the old entry in `site/keys/cl-6.conductor.json` superseded only with cl-6.maestro's agreement, since the file holds one key (check how the signer check treats a changed file first).
3. Read here: `agent.json` (state, `waiting_on`), `now.md`, `map.md`.
4. Ask cl-6.maestro (session_016CrbJLv54Kh4CSTzagW2G3, or whoever its agent.json names now) what Dinis has answered since `updated`.
5. Carry on from the first open item in `now.md`. Every commit: signed, trailers `Agent: cl-6.conductor@sgit.dinis` and `Claude-Session: <your session URL>`; `bash tools/check.sh` before every push; dev only.
