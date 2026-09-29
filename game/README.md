# Beat Eve: a key exchange game

A browser game for the key exchange and PKI material in `Chapter02(1).pptx` (CompTIA Security+ SY0-701, slides 1–40).
Open `index.html` in any modern browser. There's nothing to install and it works offline, though fonts fall back to system fonts without a connection.

Eve copies everything the player sends. The player has to get secrets to Bob anyway, using the same moves real protocols use.
Students don't memorize the hybrid key exchange diagram. They rebuild it, because every shortcut fails in front of them.

## Missions

| # | Mission | Concept | Slides |
|---|---------|---------|--------|
| 1 | Shared Secret | Symmetric encryption and the key distribution problem | 7 |
| 2 | The Big File | Hybrid key exchange (the six-step diagram) | 8, 19–21 |
| 3 | Sign It | Digital signatures: hash plus the sender's private key | 10–12 |
| 4 | Paint Lab | Diffie-Hellman key agreement (paint-mixing analogy) | 22 |
| 5 | Clock Math | DH with real modular arithmetic (p = 23, g = 5), discrete log, key length | 9, 22 |
| 6 | Breach Day | Perfect forward secrecy: static RSA exchange vs. DHE/ECDHE | 22 |
| 7 | Get Certified | CSR flow, CA vs. RA, root/intermediate/leaf chain | 33–38 |
| 8 | Checkpoint | Timed certificate validation: dates, SAN, wildcards, trust store, CRL vs. OCSP, suspension vs. revocation | 33–40 |
| 9 | Mallory in the Middle | Boss: choose the genuine certificate, then send a file that's both confidential and signed | 19–40 |

## How the courier puzzles work (missions 1–3 and 9)

Players tap items on Alice's desk to **lock** them with a key, **hash** them, or **send** them. The game tracks what Eve and Bob can open:

- a box locked with the shared key opens with the shared key
- a box locked with a public key opens only with the matching private key
- a box locked with Alice's private key opens with Alice's public key, which everyone has
- asymmetric keys refuse large files (slow, meant for small data like keys and hashes)
- sending a private key, or letting the shared key reach Eve, ends the mission with an explanation

## Classroom notes

- Each mission ends with exam-ready takeaways worded to match the slides.
- Stars (27 total) are saved in each student's browser. Nothing is sent anywhere.
- Checkpoint generates a new random set of ten certificates on every play. It works well as a warm-up, or as a competition on class score.
- Suggested order: missions 1–3 after slide 21, missions 4–6 after slide 22, missions 7–9 after slide 40.

## Why a new game

Existing options each cover a slice: Cryptris (lattice-based asymmetric crypto), Diffie-Hellman paint-mixing simulators you watch rather than play, and the pen-and-paper Security Protocol Game.
None of them walk through the Security+ sequence of hybrid exchange, signatures, PFS and PKI validation as one playable game.
