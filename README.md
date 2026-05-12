# Awesome ZKP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources for learning and building with Zero-Knowledge Proofs (ZKP).

Curated by [Oleksii Vasylenko](https://ovasylenko.com/) - available for ZK research, engineering, and consulting inquiries.

## Contents

- [Foundations & Introductions](#foundations--introductions)
- [Learning Paths](#learning-paths)
- [Math & Cryptography Prerequisites](#math--cryptography-prerequisites)
- [Key Papers & Research](#key-papers--research)
- [Proof Systems](#proof-systems)
- [Libraries & Frameworks](#libraries--frameworks)
- [Languages & DSLs](#languages--dsls)
- [Tutorials & Courses](#tutorials--courses)
- [Hands-On Labs & Exercises](#hands-on-labs--exercises)
- [Books](#books)
- [Applications & Projects](#applications--projects)
- [Developer Tools](#developer-tools)
- [Security](#security)
- [Communities & Events](#communities--events)
- [Newsletters & Media](#newsletters--media)
- [Contributing](#contributing)

---

## Foundations & Introductions

- [Zero Knowledge Proofs: An Illustrated Primer](https://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/) - Matthew Green's accessible visual introduction to ZKPs.
- [An Introduction to Zero-Knowledge Proofs in Blockchains](https://zkp.science) - Comprehensive educational resource from zkp.science.
- [Understanding ZKPs Through Simple Examples](https://vitalik.eth.limo/general/2021/01/26/snarks.html) - Vitalik Buterin's introduction to the math behind SNARKs.
- [What Are Zero-Knowledge Proofs?](https://chain.link/education/zero-knowledge-proof-zkp) - Chainlink's high-level explainer.
- [ZKProof Standards](https://zkproof.org) - Community effort to standardize ZKP technology.
- [The Incredible Machine (Avi Wigderson, 2019)](https://www.math.ias.edu/avi/book) - Foundational perspective on computational complexity and proofs.

---

## Learning Paths

### Absolute Beginner
- Start with Matthew Green's [illustrated primer](https://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/) and Chainlink's [high-level explainer](https://chain.link/education/zero-knowledge-proof-zkp).
- Watch the early [ZK Whiteboard Sessions](https://zkhack.dev/whiteboard/) modules, especially "What is a SNARK?" and "Building a SNARK".
- Read the first chapters of [The RareSkills Book of Zero Knowledge](https://www.rareskills.io/zk-book) to connect the ideas to code.
- Build a toy circuit in [Circom](https://docs.circom.io/getting-started/writing-circuits/) or [Noir](https://noir-lang.org/docs/dev/getting_started/quick_start).

### Developer Track
- Learn finite fields, arithmetic circuits, R1CS, polynomial commitments, and Fiat-Shamir.
- Build circuits with [Circom](https://docs.circom.io/) plus [snarkjs](https://github.com/iden3/snarkjs), then repeat the same idea with [Noir](https://noir-lang.org/docs).
- Complete [ZK Puzzles](https://github.com/0xPARC/zk-puzzles) and study bugs in the [ZK Bug Tracker](https://github.com/0xPARC/zk-bug-tracker).
- Try a zkVM such as [RISC Zero](https://dev.risczero.com/) or [SP1](https://docs.succinct.xyz/) once circuit-level development feels familiar.

### Research Track
- Read Justin Thaler's [Proofs, Arguments, and Zero-Knowledge](https://people.cs.georgetown.edu/jthaler/ProofsArgsAndZK.html).
- Work through sum-check, GKR, polynomial IOPs, FRI, PLONK, lookup arguments, and folding schemes.
- Follow [ZK Whiteboard Sessions](https://zkhack.dev/whiteboard/) for current topics such as lookups, folding, small fields, and lattice-based SNARKs.
- Read new papers through [IACR ePrint](https://eprint.iacr.org/) and compare constructions by assumptions, setup, proof size, verifier time, and prover cost.

### Product & Application Track
- Study privacy payments, rollups, identity, voting, storage proofs, zkML, and zk coprocessors.
- Read production docs from [Zcash](https://z.cash/), [Starknet](https://docs.starknet.io/), [Aztec](https://docs.aztec.network/), [Mina](https://docs.minaprotocol.com/), and [Semaphore](https://docs.semaphore.pse.dev/).
- Learn the security model before designing a protocol: constraints, witness generation, trusted setup, recursion, nullifiers, and public/private input boundaries.

---

## Math & Cryptography Prerequisites

- [The MoonMath Manual](https://leastauthority.com/community-matters/moonmath-manual/) - Practical math background for finite fields, elliptic curves, pairings, and SNARKs.
- [A Graduate Course in Applied Cryptography](https://toc.cryptobook.us/) - Free textbook by Boneh and Shoup; useful for modern cryptography foundations.
- [Cryptography I by Dan Boneh](https://www.coursera.org/learn/crypto) - Broad introduction to cryptographic primitives and security thinking.
- [Mathematics for Computer Science](https://ocw.mit.edu/courses/6-042j-mathematics-for-computer-science-spring-2015/) - MIT OCW course covering proofs, discrete math, probability, and number theory basics.
- [Essence of Linear Algebra](https://www.3blue1brown.com/topics/linear-algebra) - Visual refresher for vectors, matrices, bases, and transformations.
- [Abstract Algebra: Theory and Applications](http://abstract.ups.edu/) - Free book for groups, rings, fields, and homomorphisms.
- [Pairings for Beginners](https://www.craigcostello.com.au/pairings/PairingsForBeginners.pdf) - Introductory notes for bilinear pairings used in pairing-based SNARKs.

---

## Key Papers & Research

### Foundational
- [The Knowledge Complexity of Interactive Proof Systems (1985)](https://people.csail.mit.edu/silvio/Selected%20Scientific%20Papers/Proof%20Systems/The_Knowledge_Complexity_Of_Interactive_Proof_Systems.pdf) - Goldwasser, Micali, Rackoff. The paper that defined zero-knowledge proofs.
- [How to Prove Yourself: Practical Solutions to Identification and Signature Problems (1986)](https://link.springer.com/chapter/10.1007/3-540-47721-7_12) - Fiat & Shamir. Introduced the Fiat-Shamir heuristic for non-interactive proofs.
- [Computationally Sound Proofs (2000)](https://people.csail.mit.edu/silvio/Selected%20Scientific%20Papers/Proof%20Systems/Computationally_Sound_Proofs.pdf) - Micali. Foundation of succinct argument systems.

### zk-SNARKs
- [Quadratic Span Programs and Succinct NIZKs (GGPR13)](https://eprint.iacr.org/2012/215) - Key construction underlying many SNARK systems.
- [On the Size of Pairing-Based Non-Interactive Arguments (Groth16)](https://eprint.iacr.org/2016/260) - The most widely deployed SNARK proving system.
- [Succinct Non-Interactive Zero Knowledge for a von Neumann Architecture (BCTV14)](https://eprint.iacr.org/2013/879) - SNARKs for general computation.

### zk-STARKs
- [Scalable, Transparent, and Post-Quantum Secure Computational Integrity (2018)](https://eprint.iacr.org/2018/046) - Ben-Sasson et al. The original STARK paper.
- [STARKs, Part I: Proofs with Polynomials](https://vitalik.eth.limo/general/2017/11/09/starks_part_1.html) - Vitalik Buterin's three-part STARK tutorial series.

### Plonk & Universal SNARKs
- [PLONK: Permutations over Lagrange-bases for Oecumenical Noninteractive arguments of Knowledge (2019)](https://eprint.iacr.org/2019/953) - Gabizon, Williamson, Ciobotaru. Universal and updatable trusted setup.
- [Marlin: Preprocessing zkSNARKs with Universal and Updatable SRS (2019)](https://eprint.iacr.org/2019/1047) - Alternative universal SNARK construction.

### Folding Schemes
- [Nova: Recursive Zero-Knowledge Arguments from Folding Schemes (2021)](https://eprint.iacr.org/2021/370) - Kothapalli, Setty, Tzialla. Efficient incremental verifiable computation.
- [SuperNova: Proving Universal Machine Execution (2022)](https://eprint.iacr.org/2022/1758) - Extends Nova to non-uniform computation.

### Lookup Arguments
- [Plookup: A Simplified Polynomial Protocol for Lookup Tables (2020)](https://eprint.iacr.org/2020/315) - Gabizon & Williamson.
- [Lasso: A Lookup Argument with Logarithmic Proof Size (2023)](https://eprint.iacr.org/2023/1216) - Setty, Thaler, Wahby.

### Surveys
- [A Survey on the Applications of Zero-Knowledge Proofs](https://arxiv.org/abs/2408.00243) - Comprehensive overview of ZKP applications.
- [Proofs, Arguments, and Zero-Knowledge (survey)](https://people.cs.georgetown.edu/jthaler/ProofsArgsAndZK.html) - Justin Thaler's survey and textbook.

---

## Proof Systems

| System | Type | Trusted Setup | Post-Quantum | Proof Size | Prover Time |
|--------|------|---------------|--------------|------------|-------------|
| Groth16 | SNARK | Per-circuit | No | ~200 B | Fast |
| PLONK | SNARK | Universal | No | ~400 B | Moderate |
| Halo2 | SNARK | None (IPA) | No | ~5 KB | Moderate |
| STARKs | STARK | None | Yes | ~50-200 KB | Fast |
| Bulletproofs | Argument | None | No | ~700 B | Slow |

---

## Libraries & Frameworks

### Rust
- [arkworks](https://github.com/arkworks-rs) - Modular ecosystem for zkSNARK programming in Rust.
- [bellman](https://github.com/zkcrypto/bellman) - Groth16 implementation used by Zcash.
- [halo2](https://github.com/zcash/halo2) - PLONKish proving system with no trusted setup, by Zcash.
- [Plonky2](https://github.com/0xPolygonZero/plonky2) - Polygon's recursive SNARK combining PLONK and FRI.
- [Plonky3](https://github.com/Plonky3/Plonky3) - Next-generation modular toolkit for polynomial IOPs.
- [Winterfell](https://github.com/facebook/winterfell) - STARK prover/verifier by Meta.
- [lambdaworks](https://github.com/lambdaclass/lambdaworks) - Comprehensive ZKP toolkit in Rust by LambdaClass.

### C++
- [libsnark](https://github.com/scipr-lab/libsnark) - The original C++ library for zkSNARKs (R1CS-based).

### Go
- [gnark](https://github.com/Consensys/gnark) - Fast zk-SNARK library in Go by ConsensSys.

### JavaScript / TypeScript
- [snarkjs](https://github.com/iden3/snarkjs) - JavaScript implementation of Groth16 and PLONK provers/verifiers.
- [o1js](https://github.com/o1-labs/o1js) - TypeScript framework for ZK apps on Mina Protocol.

### Python
- [zksk](https://github.com/spring-epfl/zksk) - Composable zero-knowledge proofs in Python.

---

## Languages & DSLs

- [Circom](https://github.com/iden3/circom) - Domain-specific language for defining arithmetic circuits (R1CS). Widely used with snarkjs.
- [Noir](https://noir-lang.org/) - Rust-like ZK language by Aztec. Targets multiple backends.
- [Cairo](https://github.com/starkware-libs/cairo) - Language for provable programs by StarkWare. Powers Starknet.
- [ZoKrates](https://zokrates.github.io/) - High-level language and toolbox for zkSNARKs on Ethereum.
- [Leo](https://leo-lang.org/) - Functional, statically-typed language for Aleo's zkVM.
- [Lurk](https://github.com/lurk-lab/lurk-rs) - Turing-complete language for recursive zk proofs based on Lisp.

---

## Tutorials & Courses

### University Courses
- [MIT IAP 2023: Modern Zero Knowledge Cryptography](https://zkiap.com/) - Hands-on MIT course covering theory and practice.
- [UC Berkeley: Zero Knowledge Proofs](https://rdi.berkeley.edu/course/zkp/s23) - Full semester course from Berkeley RDI.
- [Stanford CS251: Cryptocurrencies and Blockchain Technologies](https://cs251.stanford.edu/) - Covers ZKPs as part of crypto curriculum.
- [Stanford CS355: Advanced Topics in Cryptography](https://crypto.stanford.edu/cs355/) - Graduate cryptography course with useful background for proof systems.
- [MIT 6.875: Cryptography and Cryptanalysis](https://ocw.mit.edu/courses/6-875-cryptography-and-cryptanalysis-spring-2005/) - Theory-heavy cryptography course for deeper foundations.

### Online Courses & Workshops
- [ZK Whiteboard Sessions](https://zkhack.dev/whiteboard) - 0xPARC's visual lecture series on ZK topics.
- [Zero Knowledge Proofs MOOC](https://docs.zkproof.org/edu) - Self-paced course from ZKProof.
- [Encode Club: ZK Bootcamp](https://www.encode.club/) - Cohort-based ZK development bootcamp.
- [Zero Knowledge Proofs Masterclass](https://101blockchains.com/masterclass/zero-knowledge-proofs/) - 101 Blockchains practical course.
- [Cyfrin Updraft: Fundamentals of Zero-Knowledge Proofs](https://www.cyfrin.io/updraft) - Beginner-friendly video course for ZK concepts and terminology.
- [Cyfrin Updraft: Noir Programming and Zero-Knowledge Circuits](https://www.cyfrin.io/updraft) - Practical Noir circuit course covering proofs, witnesses, and verifier contracts.
- [RareSkills ZK Bootcamp](https://www.rareskills.io/zk-bootcamp) - Instructor-led program for developers who want structured ZK training.

### Resource Collections
- [RareSkills ZK Book](https://www.rareskills.io/zk-book) - Practical, code-first ZK learning resource.
- [0xPARC ZK Learning Group](https://0xparc.org/blog/zk-learning-group) - Structured learning materials and group sessions.
- [Ingonyama ZKP Resources](https://www.ingonyama.com/ingopedia/zkp) - Curated video lectures and reading lists.
- [Resources for Learning Zero-Knowledge Proofs](https://dev.to/stefanalfbo/resources-for-learning-zero-knowledge-proofs-3j1j) - Community-maintained link collection.
- [CryptoCourse.dev ZK Resources](https://cryptocourse.dev/) - Curated modern cryptography resources across ZK, FHE, and MPC.
- [Class Central: Zero-Knowledge Proofs](https://www.classcentral.com/subject/zero-knowledge-proofs) - Aggregated online courses and lectures.

---

## Hands-On Labs & Exercises

### Circuits
- [Circom 2 Documentation](https://docs.circom.io/) - Official Circom docs covering signals, constraints, templates, and compiler outputs.
- [Circom: Writing Circuits](https://docs.circom.io/getting-started/writing-circuits/) - Official first-circuit tutorial.
- [Circom / snarkjs Tutorial](https://docs.iden3.io/circom-snarkjs/) - End-to-end Circom and snarkjs workflow.
- [Noir Quick Start](https://noir-lang.org/docs/dev/getting_started/quick_start) - Official guide to creating, executing, and proving Noir programs.
- [Noir Examples](https://github.com/noir-lang/noir-examples) - Example Noir projects and circuits.
- [Awesome Noir](https://github.com/noir-lang/awesome-noir) - Curated examples, libraries, tools, and learning resources for Noir.
- [ZKREPL](https://zkrepl.dev/) - Browser playground for experimenting with Circom circuits.

### Practice Problems
- [ZK Puzzles](https://github.com/0xPARC/zk-puzzles) - Circuit-writing practice problems from 0xPARC.
- [RareSkills Zero Knowledge Puzzles](https://github.com/RareSkills/zero-knowledge-puzzles) - Exercises for learning Circom syntax and EVM-compatible ZK programs.
- [ZK Bug Tracker](https://github.com/0xPARC/zk-bug-tracker) - Real ZK vulnerabilities to study and reproduce.

### zkVMs
- [RISC Zero Quickstart](https://dev.risczero.com/api/zkvm/quickstart) - Build and prove a RISC-V guest program.
- [SP1 Getting Started](https://docs.succinct.xyz/docs/sp1/getting-started/install) - Install SP1 and generate proofs for Rust programs.
- [Jolt Book](https://jolt.a16zcrypto.com/) - Documentation for a16z's lookup-based zkVM.
- [Miden VM Documentation](https://0xpolygonmiden.github.io/miden-vm/) - Learn Polygon Miden's STARK-based virtual machine.

---

## Books

- *[Proofs, Arguments, and Zero-Knowledge](https://people.cs.georgetown.edu/jthaler/ProofsArgsAndZK.html)* - Justin Thaler. The standard graduate-level textbook. Free online.
- *[The MoonMath Manual](https://leastauthority.com/community-matters/moonmath-manual/)* - Least Authority. Practical math background for ZK engineers.
- *[A Graduate Course in Applied Cryptography](https://toc.cryptobook.us/)* - Boneh & Shoup. Chapter 19+ covers ZKPs. Free online.
- *[Real-World Cryptography](https://www.manning.com/books/real-world-cryptography)* - David Wong. Includes ZKP applications in practice.
- *[The RareSkills Book of Zero Knowledge](https://www.rareskills.io/zk-book)* - Programmer-oriented path from foundational math to Groth16 and circuit development.

---

## Applications & Projects

### Layer 2 / Rollups
- [zkSync Era](https://zksync.io/) - ZK rollup by Matter Labs. General-purpose EVM-compatible L2.
- [Starknet](https://starknet.io/) - Permissionless ZK rollup by StarkWare using STARKs.
- [Polygon zkEVM](https://polygon.technology/polygon-zkevm) - EVM-equivalent ZK rollup by Polygon.
- [Scroll](https://scroll.io/) - zkEVM-based L2 with bytecode-level EVM compatibility.
- [Linea](https://linea.build/) - Consensys ZK rollup with full EVM equivalence.
- [Taiko](https://taiko.xyz/) - Based (L1-sequenced) ZK rollup.

### Privacy Chains & Protocols
- [Zcash](https://z.cash/) - Pioneer of shielded transactions using zk-SNARKs.
- [Aleo](https://aleo.org/) - Platform for private applications with built-in ZK.
- [Aztec Network](https://aztec.network/) - Privacy-first L2 with encrypted state and private execution.
- [Mina Protocol](https://minaprotocol.com/) - Constant-size (22 KB) blockchain using recursive SNARKs.
- [Penumbra](https://penumbra.zone/) - Private proof-of-stake network for Cosmos.

### Identity & Authentication
- [iden3](https://iden3.io/) - Self-sovereign identity framework using ZKPs.
- [Worldcoin](https://worldcoin.org/) - Proof-of-personhood using ZK for privacy-preserving identity.
- [Semaphore](https://semaphore.pse.dev/) - Anonymous signaling and group membership protocol.
- [Sismo](https://www.sismo.io/) - Privacy-preserving attestations using ZK badges.

### Voting & Governance
- [MACI](https://maci.pse.dev/) - Minimum Anti-Collusion Infrastructure for private on-chain voting.
- [Cicada](https://github.com/a16z/cicada) - On-chain private voting using time-lock puzzles and ZKPs.

### Decentralized Storage
- [Filecoin](https://filecoin.io/) - Decentralized storage network using ZK-based proofs of replication and space-time.

### zkVMs (Zero-Knowledge Virtual Machines)
- [RISC Zero](https://www.risczero.com/) - General-purpose zkVM based on RISC-V.
- [SP1](https://github.com/succinctlabs/sp1) - Succinct's high-performance RISC-V zkVM.
- [Jolt](https://github.com/a16z/jolt) - a16z's zkVM using lookup-based arguments (Lasso).
- [Miden](https://github.com/0xPolygonMiden/miden-vm) - Polygon's STARK-based zkVM with client-side proving.
- [Nexus](https://nexus.xyz/) - Modular, extensible, open-source zkVM.
- [Valida](https://github.com/valida-xyz/valida) - STARK-based zkVM optimized for real-world programs.

---

## Developer Tools

- [Circomspect](https://github.com/trailofbits/circomspect) - Static analysis tool for Circom circuits by Trail of Bits.
- [ECNE](https://github.com/franklynwang/ecne) - Tool for verifying correct circuit construction.
- [Halo2 Analyzer](https://github.com/quantstamp/halo2-analyzer) - Automated analysis for Halo2 circuits.
- [Sindri](https://sindri.app/) - Cloud proving infrastructure. Generate proofs via API.
- [Axiom](https://www.axiom.xyz/) - ZK coprocessor for reading on-chain data with proofs.
- [Herodotus](https://www.herodotus.dev/) - Cross-chain data access using storage proofs.

---

## Security

- [ZK Bug Tracker](https://github.com/0xPARC/zk-bug-tracker) - Public database of bugs found in ZK systems.
- [Circomspect](https://github.com/trailofbits/circomspect) - Static analyzer for finding vulnerabilities in Circom.
- [Common ZK Vulnerabilities](https://blog.trailofbits.com/2022/04/18/the-frozen-heart-vulnerability-in-plonk/) - Trail of Bits' "Frozen Heart" disclosure and analysis.
- [ZK Security Blog](https://www.zksecurity.xyz/) - Articles and security research by ZKSecurity.
- [ZK Security Audits](https://github.com/nullity00/zk-security-reviews) - Collection of public ZK audit reports.

---

## Communities & Events

### Conferences & Hackathons
- [ZK Summit](https://zkpsummit.com/) - Annual conference dedicated to zero-knowledge proofs.
- [ZK Hack](https://zkhack.dev/) - ZK-focused hackathons and educational events.
- [Real World Crypto](https://rwc.iacr.org/) - Applied cryptography conference covering ZKP advances.
- [ZKProof Workshop](https://zkproof.org) - Standards-focused community workshops.
- [ETHGlobal](https://ethglobal.com/) - Ethereum hackathons often featuring ZK tracks.

### Online Communities
- [r/Zeroknowledge](https://www.reddit.com/r/Zeroknowledge/) - Reddit community for ZK discussion.
- [Ethereum Research](https://ethresear.ch/) - Research forum with active ZK topics.
- [PSE (Privacy & Scaling Explorations)](https://pse.dev/) - Ethereum Foundation's ZK research group.
- [0xPARC](https://0xparc.org/) - Applied ZK research community.
- [ZK-Monk](https://zkmonk.org/) - ZK learning and community hub.

### Podcasts
- [Zero Knowledge Podcast](https://zeroknowledge.fm/) - Interviews with ZK researchers and builders.
- [Epicenter](https://epicenter.tv/) - Covers ZK topics in broader crypto context.

---

## Newsletters & Media

- [ZK Newsletter](https://zknewsletter.substack.com/) - Weekly roundup of ZK ecosystem news.
- [ZK Mesh](https://zkmesh.substack.com/) - Monthly newsletter on ZK developments.
- [Modular Crypto](https://modularcrypto.substack.com/) - Covers modular and ZK ecosystem updates.

---

## Contributing

Contributions are welcome! Please submit a pull request to add resources. Ensure links are active and resources are relevant to zero-knowledge proofs.

---

Last updated: May 2026.
