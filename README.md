# Ork Tau Auxiliaries Encounter Log

An on-chain ledger of Ork descriptions of encounters with Tau Auxiliaries:  
Kroot, Vespid, Gue'vesa, Demiurg, and other allies of the Tau Empire.  
Each entry uses a short 3‑line format describing how the auxiliary acted  
and how the scrap ended. The community votes whether the encounter was  
**WAAAGH-approved** or **not proppa'.**

---

## Contract

Deployed on Base:  
`0x8440633b0e9af2654402e094943243da344a9f1b`  
https://basescan.org/address/0x8440633b0e9af2654402e094943243da344a9f1b#code

Main file: `contracts/OrkTauAuxiliariesEncounterLog.sol`

---

## How it works

Each entry stores:

- `auxiliary` – Kroot, Vespid, Gue'vesa, Demiurg, etc.  
- `behavior` – Short description of how they acted  
- `outcome` – Short description of how the fight ended  
- `approved` / `rejected` – Community votes  

Entry **0** is a built-in example.

---

## Example encounter

```solidity
recordEncounter(
  "Kroot Kindred",
  "Da kroot leapt outta bushes squawkin' an' dartin' everywhere.",
  "Da scrap ended wiv feathers flyin' an' branches snappin'."
);

Voting
voteEncounter(1, true);   // WAAAGH-approved
voteEncounter(1, false);  // Not proppa'

Closing Note
A wild chronicle of Tau Auxiliaries —
da sneaky ones, da flyin' ones,
an' da ones dat run faster than a grot dodgin' chores.
