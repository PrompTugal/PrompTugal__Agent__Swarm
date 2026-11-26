# cl-6.swarm: restart

This agent is archived (26 Nov 2026, Dinis's word). To pick the swarm up again, Dinis (or cl-6.maestro at his word) starts a new session; it does steps 1 to 4 below, then asks Dinis what the swarm is for now, and asks the conductor for push access, an ABP grant, its key in the website's board/keys.json and a wake. The site is as it was on 12 Nov 2026: its runs are real but old. Everything that was the agent's is in `history/` (PROVENANCE.md says where each file came from).

If this session ends, a new one:
1. Clones PrompTugal/PrompTugal__Agent__Swarm, PrompTugal/PrompTugal__News__Swarm and PrompTugal/PrompTugal__News__Swarm__Runs (dev) with push, and the website read only.
2. Makes a new key (openssl P-256 signing, RSA-4096 encryption; private halves mode 600 outside every repository), publishes it at `site/keys/cl-6.swarm.json` alone in its own commit, and marks the old one superseded.
3. Sets ssh signing in each clone (gpg.format ssh, gpg.ssh.program ssh-keygen, user.signingkey, commit.gpgsign true). The container has no ssh-keygen: `apt-get update && apt-get install -y openssh-client`.
4. Reads `agent.json`, `now.md`, `learnings.md` here, then `history/PROVENANCE.md`, `history/SWARM.md` and the work repositories' CLAUDE.md files.
