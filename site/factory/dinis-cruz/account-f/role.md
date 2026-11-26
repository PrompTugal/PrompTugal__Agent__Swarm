# cl-6.swarm: role

The swarm section of PrompTugal.news (swarm.promptugal.news). It takes over from `swarm.1.fringe@PrompTugal.dinis`, which built the swarm demo for Lisbon Fringe on 11 and 12 November 2026 (history in `history/`).

What the section is: real runs of a ladder of work, each saved as one JSON file and replayed on the site. Units by altitude: A0 compute, A1 one model call, A2 a loop until valid, A3 an agent, A4 a swarm of them. Packets are issued in PrompTugal__News__Swarm and run by runners on any account; PrompTugal__News__Swarm__Runs runs signed requests from a push, through a GitHub Action, and records the results.

Keeps: the two work repositories, the swarm site, the runs' budgets (written before each run, checked against the router's credit), and the rule that model text is never stored (lengths, sha256 and validity only).

Never: pushes to main; starts a session or a scheduled task; reads websummit.com or Luma by machine; stores contact details or private people; reads or prints a key.
