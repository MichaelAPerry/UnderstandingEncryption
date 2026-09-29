# Understanding Encryption

Teaching materials for **CompTIA Security+ (SY0-701), Chapter 2: Cryptographic Solutions and Threats**, plus **Beat Eve**, a browser game that teaches the chapter's hardest ideas: key exchange and PKI.

## What's here

| Path | What it is |
|------|------------|
| `Chapter02(1).pptx` | Chapter 2 lecture slides (67 slides) |
| `game/index.html` | **Beat Eve**, the key exchange game (one self-contained file) |
| `game/README.md` | Teacher notes: mission-by-mission slide map and classroom tips |

## Beat Eve

> Eve copies every packet on the wire. Your job is to get secrets to Bob anyway.

Students don't memorize the hybrid key exchange diagram. They rebuild it by locking, hashing and sending items while an eavesdropper copies everything. Every shortcut fails with an explanation: sending the shared key in the open, encrypting a 2 GB file with a public key, or leaking a private key.

### Play it

- **Locally:** download or clone the repo and open `game/index.html` in any modern browser. There's nothing to install, and it runs offline.
- **On the web (GitHub Pages is on):** the game is live at
  **https://michaelaperry.github.io/UnderstandingEncryption/** — the root page redirects into the game. The game files also sit directly at `.../UnderstandingEncryption/game/`.

### Missions

| Chapter | # | Mission | Concept | Slides |
|---------|---|---------|---------|--------|
| I. The Courier | 1 | Shared Secret | Symmetric encryption, key distribution problem | 7 |
| | 2 | The Big File | Hybrid key exchange | 8, 19–21 |
| | 3 | Sign It | Digital signatures (hash + sender's private key) | 10–12 |
| II. Agree, Don't Send | 4 | Paint Lab | Diffie-Hellman key agreement | 22 |
| | 5 | Clock Math | DH with modular arithmetic, discrete log, key length | 9, 22 |
| | 6 | Breach Day | Perfect forward secrecy (DHE / ECDHE) | 22 |
| III. Who's Really Bob? | 7 | Get Certified | CSR, CA, RA, root/intermediate/leaf | 33–38 |
| | 8 | Checkpoint | Certificate validation: dates, SAN, wildcards, trust store, CRL vs. OCSP | 33–40 |
| | 9 | Mallory in the Middle | Boss: spot the fake certificate, then send secret and signed | 19–40 |
| IV. Eve's Toolkit | 10 | Chain Breaker | Blockchain tamper-evidence (real SHA-256 hash chain) | 27 |
| | 11 | Hide in Plain Sight | Obfuscation: steganography, tokenization, data masking | 24–25 |
| | 12 | Vault Keeper | TPM / HSM / enclave / escrow, KMS lifecycle, salting & key stretching | 23, 26, 29–30 |

Each mission opens with an illustrated story briefing from the cast and ends with exam-ready takeaways worded to match the slides. Stars (36 total) are saved in each student's own browser. No accounts, no tracking, and nothing leaves the page.

**Completion codes:** because progress is local, every mission win and the mission board issue codes (e.g. `M03-2-ABC123`, `R-…`) tied to the student's name. Teachers verify them on the board under "Check a student's code." **Sound:** action feedback is synthesized in-browser and can be muted with the header button.

### Suggested use

- Missions 1–3 after slide 21, missions 4–6 after slide 22, missions 7–9 after slide 40.
- **Checkpoint** deals a new random set of certificates every play, so it works as a repeatable warm-up or a class competition on score.

## License

MIT. See [LICENSE](LICENSE).
