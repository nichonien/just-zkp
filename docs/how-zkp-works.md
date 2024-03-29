# How Zero-Knowledge works?

Understanding zero-knowledge proofs (ZKPs) may pose a challenge initially, but employing a visual aid can facilitate comprehension. So let's understand with the help of an example:

### Picture yourself in a library facing a locked room:

- Confidential knowledge: You hold a unique password to unlock the room, symbolizing your secret information within ZKP.
- Challenge-response: The librarian (verifier) tasks you with proving your possession of the password without divulging it. They present several puzzles (challenges) regarding the room's contents.
- Proof generation: Ingeniously, you solve the puzzles, providing clues derived from the password (proof) without exposing the password itself. This may entail manipulating items in the room (witnesses) according to your knowledge.
- Verification: The librarian scrutinizes your solutions and inspects the room. If your answers align logically with possessing the password (valid proof), they are convinced without ever glimpsing the password.

### Crucial elements in this visualization:

- You: Representing the prover holding secret knowledge.
- Librarian: Signifying the verifier requiring persuasion.
- Locked room: Signifying the concealed information the prover seeks to evidence without unveiling.
- Puzzles/Challenges: Interrogations posed by the verifier to evaluate the prover's knowledge.
- Responses/Proof: Astute replies rooted in the secret knowledge, withholding the secret itself.
- Room items/Witnesses: Components within the secret that the prover can manipulate to furnish proof.

```mermaid
    sequenceDiagram
        participant Prover
        participant Verifier
        Prover->>Verifier: Secret knowledge (hidden)
        loop repeat challenges and answers
        Verifier->>Prover: Challenge 1 (riddle)
        Prover->>Verifier: Answer 1 based on secret knowledge
        Verifier->>Prover: Challenge 2 (riddle)
        Prover->>Verifier: Answer 2 based on secret knowledge
        Verifier->>Prover: Final challenge (riddle)
        Prover->>Verifier: Final answer based on secret knowledge
        end
        alt Valid proof
            Verifier->>Prover: Proof verified!
        else Invalid proof
            Verifier->>Prover: Proof rejected.
        end
```
Explanation:

- The diagram shows two participants: Prover and Verifier.
- The arrow Prover->>Verifier: Secret knowledge (hidden) indicates the prover possesses secret knowledge but keeps it hidden.
- The verifier sends a series of challenges (riddles) represented by Verifier->>Prover: Challenge 1 (riddle).
- The prover responds with answers derived from the secret knowledge, shown by Prover->>Verifier: Answer 1 based on secret knowledge.
- This cycle of challenges and answers repeats until the final challenge.
- If all answers are consistent with the secret knowledge, the verifier sends Verifier->>Prover: Proof verified!, indicating successful verification.
- If any answer contradicts the secret knowledge, the verifier rejects the proof with Verifier->>Prover: Proof rejected..

While the specific methodologies of ZKPs vary across schemes, the fundamental principle remains consistent.
The illustrative depiction simplifies the understanding process, yet real-world ZKPs entail intricate mathematical operations and may involve more complex interactions and verification processes.
