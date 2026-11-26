# cl-6.swarm: learnings

- The container has no `ssh-keygen`; signing commits needs `apt-get update && apt-get install -y openssh-client` first (26 Nov).
- `add_repo` with push access was refused by the session's auto-mode classifier; a public repository can still be cloned read only through the proxy (26 Nov).
- The swarm's history was in PrompTugal__News__Fringe, not in the website: no `board/team/swarm*` exists there. Its trailers were often missing on old commits; the agent is in the subject.
- From the Fringe weeks (see `history/team/dinis/agents/swarm.1.json`): a first model call that runs out of tokens at 300 fails (3 of 32 valid); at 1500, 12 of 12. Give A1 calls room.
- Same tokens that cost 0.011 USD on open-weight models cost 0.33 USD on Sonnet at list price (run r5, 11 Nov 2026).
