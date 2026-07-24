# Awesome ZKP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![Check links](https://github.com/ovasylenko/awesome-zkp/actions/workflows/links.yml/badge.svg)](https://github.com/ovasylenko/awesome-zkp/actions/workflows/links.yml)

> A curated, practical map for learning, researching, and building with zero-knowledge proofs.

Curated by [Oleksii Vasylenko](https://ovasylenko.com/) - available for ZK research, engineering, and consulting inquiries.

## How to Use This List

Zero-knowledge proofs sit at the intersection of cryptography, systems engineering, protocol design, and application development. This list is organized so you can choose the shortest useful path instead of reading everything in order.

- **New to ZK:** start with [Foundations & Introductions](#foundations--introductions), then follow the [Absolute Beginner](#absolute-beginner) learning path.
- **Building circuits or apps:** use the [Developer Track](#developer-track), then jump to [Languages & DSLs](#languages--dsls), [Hands-On Labs & Exercises](#hands-on-labs--exercises), and [Security](#security).
- **Doing research:** use the [Research Track](#research-track), then read through [Key Papers & Research](#key-papers--research) and compare systems in [Proof Systems](#proof-systems).
- **Evaluating products or protocols:** use the [Product & Application Track](#product--application-track), then review [Applications & Projects](#applications--projects), [Developer Tools](#developer-tools), and [Security](#security).

### Curation Criteria

Resources are included when they are useful, maintained, influential, or unusually clear. Preference is given to official documentation, primary research, production-grade tooling, high-signal tutorials, and security material that helps builders avoid real mistakes.

This list avoids low-effort marketing pages, shallow reposts, abandoned projects without historical importance, and duplicate resources that do not add a distinct perspective.

Project inclusion is not an endorsement or a security review. ZK software changes quickly: check release notes, audits, trusted-setup assumptions, licenses, and current network status before relying on a resource in production. Historical or sunset projects are labeled explicitly rather than presented as active choices.

Lifecycle labels are used only when an official source states the project's status: **Research**, **Alpha**, **Beta**, **Production**, **LTS**, or **Historical**. An unlabeled entry has not had its maturity independently classified; it should not be assumed production-ready.

## Contents

- [Foundations & Introductions](#foundations--introductions)
- [Learning Paths](#learning-paths)
- [Core Concepts & Vocabulary](#core-concepts--vocabulary)
- [What Counts as Zero Knowledge?](#what-counts-as-zero-knowledge)
- [Choosing a Development Approach](#choosing-a-development-approach)
- [Math & Cryptography Prerequisites](#math--cryptography-prerequisites)
- [Key Papers & Research](#key-papers--research)
- [Research Frontiers](#research-frontiers)
- [Proof Systems](#proof-systems)
- [Trusted Setup & Ceremonies](#trusted-setup--ceremonies)
- [Benchmarks & Comparisons](#benchmarks--comparisons)
- [Libraries & Frameworks](#libraries--frameworks)
- [Languages & DSLs](#languages--dsls)
- [Tutorials & Courses](#tutorials--courses)
- [Hands-On Labs & Exercises](#hands-on-labs--exercises)
- [Client-Side & Mobile Proving](#client-side--mobile-proving)
- [Books](#books)
- [Applications & Projects](#applications--projects)
- [Developer Tools](#developer-tools)
- [Verification & Aggregation](#verification--aggregation)
- [Hardware Acceleration](#hardware-acceleration)
- [Testing & Validation](#testing--validation)
- [Security](#security)
- [Communities & Events](#communities--events)
- [Newsletters & Media](#newsletters--media)
- [More Curated Lists](#more-curated-lists)
- [Contributing](#contributing)

---

## Foundations & Introductions

- [Zero Knowledge Proofs: An Illustrated Primer](https://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/) - Matthew Green's accessible visual introduction to ZKPs.
- [An Introduction to Zero-Knowledge Proofs in Blockchains](https://zkp.science) - Comprehensive educational resource from zkp.science.
- [Understanding ZKPs Through Simple Examples](https://vitalik.eth.limo/general/2021/01/26/snarks.html) - Vitalik Buterin's introduction to the math behind SNARKs.
- [What Are Zero-Knowledge Proofs?](https://chain.link/education/zero-knowledge-proof-zkp) - Chainlink's high-level explainer.
- [ZKProof Standards](https://zkproof.org) - Community effort to standardize ZKP technology.
- [ZKDocs](https://www.zkdocs.com/) - Trail of Bits' detailed, security-focused documentation for ZK protocols and primitives.
- [NIST Privacy-Enhancing Cryptography: ZKP](https://csrc.nist.gov/projects/pec/zkproof) - NIST standards initiative and threshold-scheme track for ZK proofs.
- [The Incredible Machine (Avi Wigderson, 2019)](https://www.math.ias.edu/avi/book) - Foundational perspective on computational complexity and proofs.

---

## Learning Paths

### Absolute Beginner
Use this path if you want the intuition first and the math later.

- Start with Matthew Green's [illustrated primer](https://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/) and Chainlink's [high-level explainer](https://chain.link/education/zero-knowledge-proof-zkp).
- Watch the early [ZK Whiteboard Sessions](https://zkhack.dev/whiteboard/) modules, especially "What is a SNARK?" and "Building a SNARK".
- Read the first chapters of [The RareSkills Book of Zero Knowledge](https://www.rareskills.io/zk-book) to connect the ideas to code.
- Build a toy circuit in [Circom](https://docs.circom.io/getting-started/writing-circuits/) or [Noir](https://noir-lang.org/docs/dev/getting_started/quick_start).

### Developer Track
Use this path if you can already code and want to build working proofs.

- Learn finite fields, arithmetic circuits, R1CS, polynomial commitments, and Fiat-Shamir.
- Build circuits with [Circom](https://docs.circom.io/) plus [snarkjs](https://github.com/iden3/snarkjs), then repeat the same idea with [Noir](https://noir-lang.org/docs).
- Complete [ZK Puzzles](https://github.com/0xPARC/zk-puzzles) and study bugs in the [ZK Bug Tracker](https://github.com/0xPARC/zk-bug-tracker).
- Try a zkVM such as [RISC Zero](https://dev.risczero.com/) or [SP1](https://docs.succinct.xyz/) once circuit-level development feels familiar.

### Research Track
Use this path if you want to understand proof systems from first principles.

- Read Justin Thaler's [Proofs, Arguments, and Zero-Knowledge](https://people.cs.georgetown.edu/jthaler/ProofsArgsAndZK.html).
- Work through sum-check, GKR, polynomial IOPs, FRI, PLONK, lookup arguments, and folding schemes.
- Follow [ZK Whiteboard Sessions](https://zkhack.dev/whiteboard/) for current topics such as lookups, folding, small fields, and lattice-based SNARKs.
- Read new papers through [IACR ePrint](https://eprint.iacr.org/) and compare constructions by assumptions, setup, proof size, verifier time, and prover cost.

### Product & Application Track
Use this path if you need to evaluate where ZK is useful, risky, or production-ready.

- Study privacy payments, rollups, identity, voting, storage proofs, zkML, and zk coprocessors.
- Read production docs from [Zcash](https://z.cash/), [Starknet](https://docs.starknet.io/), [Aztec](https://docs.aztec.network/), [Mina](https://docs.minaprotocol.com/), and [Semaphore](https://docs.semaphore.pse.dev/).
- Learn the security model before designing a protocol: constraints, witness generation, trusted setup, recursion, nullifiers, and public/private input boundaries.

---

## Core Concepts & Vocabulary

- **Statement / public inputs:** the claim visible to the verifier, such as a Merkle root, commitment, or program output.
- **Witness / private inputs:** secret data used by the prover to establish the statement.
- **Arithmetization:** the representation of computation as algebraic constraints, such as R1CS, AIR, or a PLONKish circuit.
- **Polynomial commitment scheme (PCS):** a primitive used to commit to polynomials and later prove evaluation claims; common families include KZG, IPA, and FRI.
- **Trusted setup:** generation of public parameters that may be circuit-specific or universal. Some systems are transparent and need no secret setup ceremony.
- **Recursion:** verifying one proof inside another proof, commonly used for aggregation and compression.
- **Folding / IVC:** incrementally combining computation steps or constraint instances without generating a complete recursive proof after every step.
- **zkVM:** a virtual machine whose execution can be proven. It trades some circuit-level control for a more familiar programming model.

## What Counts as Zero Knowledge?

A proof system has three separate properties that should not be conflated:

- **Completeness:** an honest prover with a valid witness can convince the verifier.
- **Soundness:** a cheating prover cannot convince the verifier of a false statement, except with negligible probability.
- **Zero knowledge:** the proof reveals nothing about the witness beyond the truth of the public statement.

A cryptographic **proof** is sound against an unbounded prover; an **argument** relies on computational assumptions and is sound against efficient adversaries. Most deployed SNARKs and STARKs are arguments, despite the ecosystem's common use of “proof” as an umbrella term.

Succinctness does not imply privacy. A validity proof can establish correct execution while exposing the full trace or all inputs, and many zkVM or STARK stacks make zero-knowledge blinding optional for performance. Likewise, a **zkVM** is an execution environment, not a single proof system. When evaluating a project, verify whether zero knowledge is inherent, optional, disabled in the cited configuration, or not provided at all.

## Choosing a Development Approach

| Goal | Start with | Why | Main trade-off |
|------|------------|-----|----------------|
| Learn circuit design | Circom, Noir, or gnark | Makes constraints, witnesses, and public inputs concrete | You must reason carefully about under-constraint and field arithmetic |
| Prove an existing Rust program | RISC Zero, SP1, Jolt, or OpenVM | Familiar language and tooling; less custom circuit work | More proving overhead and a larger trusted computing stack |
| Build a highly specialized prover | Halo2, arkworks, Plonky3, or Winterfell | Fine-grained control over arithmetization and performance | Steeper cryptography and systems learning curve |
| Prove repeated or stateful computation | Nova-family folding schemes or an IVC framework | Efficient incremental composition | Rapidly evolving APIs and more complex soundness assumptions |
| Add private membership or signaling | Semaphore or MACI | Reusable application protocols with defined threat models | Protocol constraints may not fit every identity or governance model |

Before choosing, compare the security assumptions, setup model, supported fields and curves, recursion strategy, proof size, verifier environment, prover memory, hardware requirements, audit history, and license. Benchmark on your own workload: published numbers rarely use identical circuits, security levels, hardware, or proof configurations.

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

For a chronological explanation of how the main constructions fit together, see [A Research History of Zero-Knowledge Proofs](docs/research-history.md). It covers foundations, PCPs and sum-check, pairing SNARKs, universal setups, transparent arguments, STARKs, recursion, folding, MPC-in-the-head, lattice-based ZK, and key limitations.

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
- [Zero-Knowledge Proof Frameworks: A Systematic Survey](https://arxiv.org/abs/2502.07063) - 2025 comparison of practical frameworks, development models, and application trade-offs.
- [Proofs, Arguments, and Zero-Knowledge (survey)](https://people.cs.georgetown.edu/jthaler/ProofsArgsAndZK.html) - Justin Thaler's survey and textbook.

---

## Research Frontiers

### Recursion & Folding
- [HyperNova: Recursive Arguments for Customizable Constraint Systems (2023)](https://eprint.iacr.org/2023/573) - Generalizes folding schemes for customizable constraint systems.
- [ProtoStar: Generic Efficient Accumulation/Folding for Special Sound Protocols (2023)](https://eprint.iacr.org/2023/620) - Folding and accumulation framework for special-sound protocols.
- [CycleFold: Folding-scheme-based Recursive Arguments over a Cycle of Elliptic Curves (2023)](https://eprint.iacr.org/2023/1192) - Recursive proof construction using elliptic-curve cycles.
- [ProtoGalaxy: Efficient ProtoStar-style Folding of Multiple Instances (2023)](https://eprint.iacr.org/2023/1106) - Multi-instance folding for reducing recursive proving overhead.
- [LatticeFold: A Lattice-based Folding Scheme and its Applications to Succinct Proof Systems (2024)](https://eprint.iacr.org/2024/257) - Folding scheme built from lattice assumptions.
- [Mira: Efficient Folding for Pairing-based Arguments (2024)](https://eprint.iacr.org/2024/2025) - Beal & Fisch. Pairing-friendly folding with efficient accumulation.

### Lookups, zkVMs & General-Purpose Proving
- [Jolt: SNARKs for Virtual Machines via Lookups (2023)](https://eprint.iacr.org/2023/1217) - Lookup-based approach for proving virtual-machine execution.
- [Binius: Highly Efficient Proofs over Binary Fields (2023)](https://eprint.iacr.org/2023/1784) - Binary-field proof system design aimed at high prover efficiency.
- [Caulk: Lookup Arguments in Sublinear Time (2022)](https://eprint.iacr.org/2022/621) - Lookup argument with sublinear proving and verification techniques.
- [Orion: Zero Knowledge Proof with Linear Prover Time (2022)](https://eprint.iacr.org/2022/1010) - Linear-time prover construction for transparent arguments.

### Polynomial Commitments & SNARK Building Blocks
- [Bulletproofs: Short Proofs for Confidential Transactions and More (2017)](https://eprint.iacr.org/2017/1066) - Inner-product argument foundation for many transparent proof systems.
- [DARK: Practical Non-Interactive Zero-Knowledge Proofs from Class Groups (2019)](https://eprint.iacr.org/2019/1229) - Transparent polynomial commitments from groups of unknown order.
- [Hyrax: Doubly-efficient zkSNARKs without Trusted Setup (2017)](https://eprint.iacr.org/2017/1132) - Doubly efficient proof system without trusted setup.
- [Brakedown: Linear-time and Field-agnostic SNARKs for R1CS (2021)](https://eprint.iacr.org/2021/1043) - Linear-time prover with field-agnostic commitments.
- [HybridPlonk: SubLogarithmic Linear Time SNARKs from Improved Sum-Check (2025)](https://eprint.iacr.org/2025/908) - Singh, Patranabis & Sinha. Faster SNARKs via improved sum-check protocols.
- [Garuda and Pari: Faster and Smaller SNARKs via Equifficient Polynomial Commitments (2024)](https://eprint.iacr.org/2024/1245) - Dellepere, Mishra & Shirzad. Compact SNARKs from new commitment schemes.
- [Zeromorph: Zero-Knowledge Multilinear-Evaluation Proofs from Homomorphic Univariate Commitments (2024)](https://eprint.iacr.org/2023/917) - Kohrita & Towa. Multilinear commitments with constant proof size.

### zkML & Verifiable AI
- [zkLLM: Zero Knowledge Proofs for Large Language Models (2024)](https://arxiv.org/abs/2406.09032) - Proving LLM inference with succinct verification.
- [ZKTorch: Compiling ML Inference to Zero-Knowledge Proofs via Parallel Proof Accumulation (2025)](https://arxiv.org/abs/2507.07031) - Parallel proof accumulation for ONNX model inference.

### ZK on Bitcoin
- [Applications Of Zero-Knowledge Proofs On Bitcoin (2025)](https://eprint.iacr.org/2025/1271) - Protocols for proof-of-reserve, light clients, and private rollups on Bitcoin.

---

## Proof Systems

These are families, not directly comparable products. Concrete proof size and performance depend on the implementation, security level, arithmetization, commitment scheme, recursion, and workload.

| Family | Typical representation / commitment | Setup | Quantum-resistance posture | Common fit |
|--------|-------------------------------------|-------|----------------------------|------------|
| Groth16 | QAP/R1CS with pairing-based commitments | Circuit-specific ceremony | Not post-quantum | Very small proofs and inexpensive on-chain verification for stable circuits |
| PLONKish | Polynomial IOP with custom gates and lookups; KZG or IPA backends | Universal/updatable with KZG; transparent with IPA | Common backends are not post-quantum | Flexible application circuits, rollups, and recursive constructions |
| STARK / FRI | AIR with hash-based commitments and FRI | Transparent | Designed around hash-based assumptions commonly considered post-quantum | Large computations, transparent proving, and recursion where larger proofs are acceptable |
| Bulletproofs | R1CS and inner-product arguments | Transparent | Not post-quantum | Range proofs and smaller statements without a trusted setup |
| Folding / IVC | Relaxed R1CS, CCS, or related instances; commitment varies | Varies by construction | Varies by construction | Incremental, recursive, and stateful computation |

Do not infer security from the family name alone. For example, “PLONK” does not specify the commitment scheme, transcript, curve, lookup argument, or implementation, and “zkVM” describes an execution model rather than one proof system.

---

## Trusted Setup & Ceremonies

A structured reference string (SRS) may be circuit-specific, universal and updatable, or absent in transparent systems. For multi-party ceremonies, security generally depends on at least one participant generating and destroying their secret contribution correctly. Development parameters or locally generated “toxic waste” must never secure production proofs.

- [Perpetual Powers of Tau](https://pse.dev/projects/powers-of-tau) - **LTS.** PSE's ongoing phase-one ceremony for circuits up to `2^28` constraints.
- [Circom: Proving Circuits with ZK](https://docs.circom.io/getting-started/proving-circuits/) - Practical Groth16 phase-one and circuit-specific setup workflow with snarkjs.
- [SoK: Trusted Setups for Powers-of-Tau Strings](https://eprint.iacr.org/2025/064) - Systematization of setup constructions, security properties, and ceremony trade-offs.
- [On-Chain Trusted Setup Ceremony](https://a16zcrypto.com/posts/article/on-chain-trusted-setup-ceremony/) - Explanation and implementation of an auditable EVM-based Powers-of-Tau ceremony.

Before consuming an SRS, verify its maximum degree, curve, transcript, contribution-validation procedure, final artifact hashes, and whether the application requires a second circuit-specific phase.

---

## Benchmarks & Comparisons

- [zkbench](https://zkbench.dev/) - Benchmarks and comparison data for zero-knowledge proof systems.
- [zk-Harness](https://github.com/zkCollective/zk-Harness) - Benchmarking framework for general-purpose ZK languages and libraries.
- [Delendum ZK Benchmarking](https://github.com/delendum-xyz/zk-benchmarking) - Benchmark suite for comparing ZK proof libraries across standardized tasks.
- [babybear-labs ZK Benchmark](https://github.com/babybear-labs/benchmark) - Benchmark implementations for zkVMs and proving systems including RISC Zero, SP1, Jolt, Halo2, Circom, and powdr.
- [zkInterface](https://github.com/QED-it/zkinterface) - Interoperability format for exchanging constraint systems between ZK tools.

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
- [Barretenberg](https://barretenberg.aztec.network/docs/) - Aztec's C++ proving library and cryptographic backend for Noir.

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
- [The halo2 Book](https://zcash.github.io/halo2/) - Official guide to Halo2 concepts, circuit development, and crate usage.
- [gnark Documentation](https://docs.gnark.consensys.io/) - Official guides, concepts, reference material, and playground for writing zkSNARK circuits in Go.
- [ZKREPL](https://zkrepl.dev/) - Browser playground for experimenting with Circom circuits.

### Practice Problems
- [ZK Puzzles](https://github.com/0xPARC/zk-puzzles) - Circuit-writing practice problems from 0xPARC.
- [RareSkills Zero Knowledge Puzzles](https://github.com/RareSkills/zero-knowledge-puzzles) - Exercises for learning Circom syntax and EVM-compatible ZK programs.
- [ZK Bug Tracker](https://github.com/0xPARC/zk-bug-tracker) - Real ZK vulnerabilities to study and reproduce.

### zkVMs
- [RISC Zero Quickstart](https://dev.risczero.com/api/zkvm/quickstart) - Build and prove a RISC-V guest program.
- [SP1 Getting Started](https://docs.succinct.xyz/docs/sp1/getting-started/install) - Install SP1 and generate proofs for Rust programs.
- [Jolt Book](https://jolt.a16zcrypto.com/) - Documentation for a16z's lookup-based zkVM.
- [Miden VM Documentation](https://docs.miden.xyz/design/) - Design reference for Miden's STARK-based VM, proving system, and execution model.
- [OpenVM Documentation](https://docs.openvm.dev/) - Build and customize programs with OpenVM's modular zkVM framework.

---

## Client-Side & Mobile Proving

Client-side proving keeps witnesses on the user's device, but memory limits, binary size, battery use, browser isolation, and platform-specific acceleration become part of the security and usability model.

- [Mopro](https://github.com/zkmopro/mopro) - Toolkit and generated bindings for Circom, Halo2, and Noir proving on iOS, Android, React Native, Flutter, and the web.
- [NoirJS Browser App Tutorial](https://noir-lang.org/docs/tutorials/noirjs_app/) - Generate witnesses and proofs in a browser with NoirJS and Barretenberg's WASM backend.
- [snarkjs in the Browser](https://github.com/iden3/snarkjs#in-the-browser) - JavaScript and WebAssembly tooling for client-side Groth16 and PLONK workflows.

For production apps, test peak memory rather than average memory, bind every proof to its application and network context, avoid logging private inputs, and verify proofs independently of the device that generated them.

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
- [Scroll](https://scroll.io/) - zkEVM-based L2 with bytecode-level EVM compatibility.
- [Linea](https://linea.build/) - Consensys ZK rollup with full EVM equivalence.
- [Taiko](https://taiko.xyz/) - Based (L1-sequenced) ZK rollup.

### Privacy Chains & Protocols
- [Zcash](https://z.cash/) - Pioneer of shielded transactions using zk-SNARKs.
- [Aleo](https://aleo.org/) - Platform for private applications with built-in ZK.
- [Aztec Network](https://aztec.network/) - Privacy-first L2 with encrypted state and private execution.
- [Mina Protocol](https://minaprotocol.com/) - Constant-size (22 KB) blockchain using recursive SNARKs.
- [Penumbra](https://penumbra.zone/) - Private proof-of-stake network for Cosmos.
- [zkBob](https://docs.zkbob.com/) - Compliance-oriented private-transfer protocol and wallet; check the deployment pages because supported pools have changed over time.

### Identity & Authentication
- [iden3](https://iden3.io/) - Self-sovereign identity framework using ZKPs.
- [World ID](https://docs.world.org/world-id) - Proof-of-human protocol that uses ZK proofs for unlinkable presentation of credentials.
- [Semaphore](https://semaphore.pse.dev/) - Anonymous signaling and group membership protocol.
- [Longfellow ZK](https://github.com/google/longfellow-zk) - **Security review.** Google's library for ZK protocols over MDOC, JWT, and W3C Verifiable Credential identity formats.

### Voting & Governance
- [MACI](https://maci.pse.dev/) - Minimum Anti-Collusion Infrastructure for private on-chain voting.
- [Cicada](https://github.com/a16z/cicada) - On-chain private voting using time-lock puzzles and ZKPs.

### Decentralized Storage
- [Filecoin](https://filecoin.io/) - Decentralized storage network using ZK-based proofs of replication and space-time.

### zkVMs (Zero-Knowledge Virtual Machines)
- [RISC Zero](https://www.risczero.com/) - General-purpose zkVM based on RISC-V.
- [SP1](https://github.com/succinctlabs/sp1) - Succinct's high-performance RISC-V zkVM.
- [Jolt](https://github.com/a16z/jolt) - a16z's zkVM using lookup-based arguments (Lasso).
- [Miden VM](https://github.com/0xMiden/miden-vm) - **Alpha.** STARK-based virtual machine used by Miden's client-side proving architecture; not production-ready.
- [OpenVM](https://github.com/openvm-org/openvm) - Modular zkVM framework designed for custom instruction sets and application-specific extensions.
- [Nexus](https://nexus.xyz/) - Modular, extensible, open-source zkVM.
- [Valida](https://github.com/valida-xyz/valida) - STARK-based zkVM optimized for real-world programs.
- [ZisK](https://github.com/0xPolygonHermez/zisk) - Open-source RISC-V zkVM focused on high-throughput proof generation.
- [ZKM](https://github.com/zkMIPS/zkm) - MIPS32r2-based zkVM and proving stack.

### ZK on Bitcoin
- [Citrea](https://docs.citrea.xyz/) - EVM-compatible ZK rollup that uses Bitcoin for data availability and a BitVM-based bridge design.
- [BitcoinOS](https://bitcoinos.dev/) - Project developing BitSNARK-based verification and rollup infrastructure for Bitcoin.
- [ZeroSync](https://zerosync.org/) - STARK-based ZK light client for Bitcoin header-chain verification.
- [BitVM](https://bitvm.org/) - Optimistic verification paradigm for expressive computation on Bitcoin via fraud proofs.

### zkML & Verifiable Compute
- [EZKL](https://docs.ezkl.xyz/) - Toolchain for proving machine-learning and ONNX computational graph inference with ZK proofs.
- [Giza](https://www.gizatech.xyz/) - ML platform on Starknet for verifiable AI agents and autonomous DeFi strategies.
- [Polyhedra](https://polyhedra.network/) - zkPyTorch compiler and Expander proof system for verifiable ML and cross-chain zkBridge.
- [Modulus Labs](https://www.modulus.xyz/) - Specialized ZK proofs for AI inference; built RockyBot and zkPredictor.
- [Rarimo](https://rarimo.com/) - Bionetta proving framework for client-side zkML (e.g., face recognition) in zkPassport.

### Web Data & Attestations
- [TLSNotary](https://tlsnotary.org/docs/intro) - Protocol for privacy-preserving provenance and selective disclosure of HTTPS data.
- [ZK Email](https://github.com/zkemail) - Tooling for proving facts about DKIM-signed emails while selectively revealing content.
- [ZKPassport](https://zkpassport.id/) - Private identity verification from biometric passports using zero-knowledge proofs.
- [Rarimo ZK Passport](https://docs.rarimo.com/zk-passport/) - Turn biometric passports into flexible ZK identity credentials for Web3.

### ZK Bridges & Interoperability
- [Polyhedra zkBridge](https://polyhedra.network/zkbridge) - zk-SNARK-based cross-chain state and message verification.
- [Union](https://union.build/) - ZK-powered cross-chain consensus verification supporting Solidity, Move, Cosmos, and BitVM.

### Historical & Sunset Projects

- [Polygon zkEVM Mainnet Beta](https://polygon.technology/polygon-zkevm) - **Historical.** EVM-equivalent rollup whose sequencer was sunset on July 3, 2026; retained for its technical and ecosystem history.
- [Sismo](https://github.com/sismo-core) - **Historical.** ZK badge and selective-disclosure protocol whose public repositories remain useful as implementation references.

---

## Developer Tools

- [Circomspect](https://github.com/trailofbits/circomspect) - Static analysis tool for Circom circuits by Trail of Bits.
- [ECNE](https://github.com/franklynwang/ecne) - Tool for verifying correct circuit construction.
- [Halo2 Analyzer](https://github.com/quantstamp/halo2-analyzer) - Automated analysis for Halo2 circuits.
- [Sindri](https://sindri.app/) - Cloud proving infrastructure. Generate proofs via API.
- [Axiom](https://www.axiom.xyz/) - ZK coprocessor for reading on-chain data with proofs.
- [Herodotus](https://www.herodotus.dev/) - Cross-chain data access using storage proofs.
- [Brevis](https://brevis.network/) - ZK data coprocessor for omnichain historical data and verifiable compute.
- [Lagrange](https://lagrange.dev/) - ZK coprocessor with DeepProve library for verifiable ML and cross-chain state.

## Verification & Aggregation

- [Nebra UPA](https://nebra.one/) - Universal proof-aggregation protocol for amortizing on-chain verification costs.
- [Aligned Proof Aggregation](https://docs.alignedlayer.com/architecture/2_aggregation_mode) - Recursive aggregation service that compresses supported proofs before Ethereum verification.
- [zkVerify](https://docs.zkverify.io/handbook/introduction/what-is-zkverify) - Dedicated verification chain with proof-system-specific verifier modules and aggregated verification receipts.
- [snarkjs Solidity Verifier](https://docs.circom.io/getting-started/proving-circuits/#verifying-from-a-smart-contract) - Generate and exercise a circuit-specific Groth16 verifier contract.
- [gnark Verifier Support](https://github.com/Consensys/gnark#supported-proving-systems-and-curves) - Exports audited Groth16 and PLONK verifier templates for supported curves, with BN254 as the primary Solidity target.

Verification infrastructure changes the trust boundary. Check which proof systems and versions are accepted, how verification keys are registered, how public inputs are committed, whether aggregation is cryptographic or crypto-economic, how inclusion is proven, and where data remains available.

## Hardware Acceleration

- [Ingonyama ICICLE](https://github.com/ingonyama-zk/icicle) - GPU-accelerated cryptography library (MSM, NTT, Poseidon) with Rust and Go bindings.
- [Cysic](https://cysic.xyz/) - GPU and custom-hardware acceleration platform for ZK proving.
- [Fabric Cryptography](https://www.fabriccryptography.com/) - Verifiable Processing Unit (VPU) custom chip for ZK, FHE, and MPC.
- [Supranational](https://www.supranational.net/) - GPU-accelerated ZK proving infrastructure and optimized cryptographic implementations.
- [Irreducible](https://www.irreducible.com/) - FPGA and zkASIC hardware combining Binius-style proofs with custom silicon.

---

## Testing & Validation

- [Circom: Testing Circuits](https://docs.circom.io/getting-started/testing-circuits/) - Official workflow for writing and running circuit tests.
- [gnark Testing and Security](https://github.com/Consensys/gnark#testing) - Examples of release checks, fuzz tests, verifier tests, audits, and published security advisories.
- [CIVER](https://github.com/costa-group/circom_civer) - Modular verification of Circom safety properties and tag assertions.

Minimum validation should include positive tests, invalid-witness tests, mutated public inputs, boundary and out-of-range values, alternate witnesses for the same statement, malformed proof encodings, wrong verification keys, wrong domains or chain IDs, replay attempts, and differential checks between native witness logic and circuit constraints.

For benchmarks, publish the exact commit, security parameters, circuit or guest workload, proof mode, hardware, thread count, accelerator, warm-up policy, peak memory, proof size, verifier environment, and whether setup or compilation time is included.

---

## Security

### Vulnerability Databases & Audit References
- [ZK Bug Tracker](https://github.com/0xPARC/zk-bug-tracker) - Public database of bugs found in ZK systems.
- [Trail of Bits ZK Blog](https://blog.trailofbits.com/categories/zero-knowledge/) - Security research, vulnerability writeups, and tooling updates for ZK systems.
- [Veridise: What Do ZK Developers Get Wrong?](https://veridise.com/blog/learn-blockchain/lessons-from-the-auditing-trenches-what-do-zk-developers-get-wrong/) - Audit-driven examples of missing constraints, protocol mismatches, and application-layer ZK bugs.
- [Zellic: What Is a ZK Audit?](https://www.zellic.io/blog/what-is-a-zk-audit) - Practical overview of how auditors review ZK protocol design, circuits, and integrations.

### Static Analysis & Formal Verification
- [Circomspect](https://github.com/trailofbits/circomspect) - Static analyzer for finding vulnerabilities in Circom.
- [Picus](https://docs.veridise.tools/picus-v2) - Formal verification tool for detecting nondeterministic and under-constrained ZK circuits.
- [ZK Vanguard](https://docs.audithub.dev/zkvanguard/) - Static analysis platform for detecting ZK circuit issues such as unconstrained signals and nondeterministic witness code.

### Known Vulnerability Classes
- [Common ZK Vulnerabilities](https://blog.trailofbits.com/2022/04/18/the-frozen-heart-vulnerability-in-plonk/) - Trail of Bits' "Frozen Heart" disclosure and analysis.
- [ZK Security Blog](https://www.zksecurity.xyz/) - Articles and security research by ZKSecurity.
- [ZK Security Audits](https://github.com/nullity00/zk-security-reviews) - Collection of public ZK audit reports.
- [ZKDocs Security](https://www.zkdocs.com/docs/zkdocs/security-of-zkps/) - Practical notes on ZK protocol security assumptions, pitfalls, and misuse cases.
- [Frozen Heart Coordinated Disclosure](https://blog.trailofbits.com/2022/04/13/part-1-coordinated-disclosure-of-vulnerabilities-affecting-girault-bulletproofs-and-plonk/) - Fiat-Shamir implementation failures that affected Girault, Bulletproofs, PlonK, SnarkJS, gnark, and other implementations.
- [It Pays to Be Circomspect](https://blog.trailofbits.com/2022/09/15/it-pays-to-be-circomspect/) - Trail of Bits' introduction to Circomspect and the Tornado Cash-style missing-constraint failure mode.
- [Zcash Counterfeiting Vulnerability](https://z.cash/zcash-counterfeiting-vulnerability-successfully-remediated/) - Postmortem on a soundness bug that could have allowed undetectable counterfeiting before Sapling.
- [Hacking Underconstrained Circom Circuits](https://rareskills.io/post/underconstrained-circom) - Hands-on walkthrough of exploiting unconstrained Circom witnesses.
- [Compute Then Constrain](https://rareskills.io/post/compute-then-constrain) - Practical Circom pattern for using hints safely by explicitly constraining computed signals.

### Security Research Papers
- [Automated Detection of Underconstrained Circuits for Zero-Knowledge Proofs](https://eprint.iacr.org/2023/512) - PLDI 2023 paper behind Picus/QED2; detects non-unique witnesses in Circom/R1CS-style circuits.
- [Automated Verification of Consistency in Zero-Knowledge Proof Circuits](https://eprint.iacr.org/2025/916) - CAV 2025 work on checking consistency between witness generators and arithmetic circuits.
- [Certifying Zero-Knowledge Circuits with Refinement Types](https://eprint.iacr.org/2023/547) - Introduces Coda, a refinement-typed language for specifying and checking ZK application properties.
- [Formal Verification of Zero-Knowledge Circuits](https://arxiv.org/abs/2311.08858) - ACL2-based framework for verifying R1CS and prime-field constraint systems.
- [Compositional Formal Verification of Zero-Knowledge Circuits](https://eprint.iacr.org/2023/1278) - Applies compositional theorem proving to R1CS gadgets generated by Aleo's snarkVM.
- [Full Proof Cryptography: Verifiable Compilation of Efficient Zero-Knowledge Protocols](https://www.microsoft.com/en-us/research/publication/full-proof-cryptography-verifiable-compilation-of-efficient-zero-knowledge-protocols/) - CCS 2012 paper on ZKCrypt and verified compilation for zero-knowledge proofs of knowledge.
- [CirC: Compiler Infrastructure for Proof Systems, Software Verification, and More](https://doi.org/10.1109/SP46214.2022.9833782) - IEEE S&P 2022 compiler infrastructure connecting proof systems, circuits, and software verification.
- [SoK: Zero-Knowledge Range Proofs](https://eprint.iacr.org/2024/430) - Systematization of range-proof constructions and their trade-offs for application designers.

### Bad Patterns to Watch For
- **Under-constrained circuits:** missing business-logic constraints, unconstrained outputs, unused subcomponents, or assuming helper functions enforce constraints.
- **Assignment mistaken for constraint:** using witness-generation hints such as Circom `<--` without adding matching constraints.
- **Missing range and bit-length checks:** forgetting that arithmetic happens modulo the scalar field, especially around comparisons, overflows, nullifiers, Merkle inputs, and Solidity `uint256` values.
- **Nondeterministic witnesses:** allowing multiple valid witnesses for the same public statement, commonly in nullifier, commitment, or parsing logic.
- **Unbound public inputs:** accepting public inputs, verification keys, domains, chain IDs, roots, or application context that are not bound into the circuit, transcript, or verifier.
- **Broken Fiat-Shamir transcripts:** omitting public statement values, commitments, domain separators, or protocol parameters from challenge derivation.
- **Verifier integration gaps:** failing to check proof-system field bounds, proof/verifying-key identity, replay protection, nullifier reuse, root freshness, or contract-level authorization.
- **Trusted setup assumptions:** treating toxic-waste compromise, ceremony provenance, or circuit upgrades as operational details instead of security-critical protocol assumptions.
- **Privacy leakage by visibility:** exposing witness-derived values as public signals, logs, calldata, events, or reusable identifiers.
- **Only testing happy paths:** lacking negative tests that mutate witnesses, public inputs, roots, nullifiers, proof bytes, and verifier parameters.

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
- [Paradigm: Hardware Acceleration for ZK Proofs](https://www.paradigm.xyz/2022/04/zk-hardware) - Deep dive into GPU, FPGA, and ASIC acceleration for ZK provers.

---

## More Curated Lists

- [a16z crypto Canon: Zero Knowledge Proofs](https://a16zcrypto.com/posts/article/zero-knowledge-canon/) - Curated conceptual reading path from a16z crypto.
- [Matter Labs Awesome Zero Knowledge Proofs](https://github.com/matter-labs/awesome-zero-knowledge-proofs) - Large historical awesome list of ZK papers, libraries, and learning resources.
- [0xPARC Learning Resources](https://learn.0xparc.org/) - Applied ZK learning hub from the 0xPARC ecosystem.
- [ZKProof Community Reference](https://docs.zkproof.org/reference) - Community reference material around ZK terminology, standards, and education.

---

## Contributing

Contributions are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) and the [Code of Conduct](CODE_OF_CONDUCT.md) before opening a pull request. Additions must explain their distinct value, cite a primary source, disclose lifecycle and security status when known, and pass the automated link check.

This list is released under [CC0 1.0 Universal](LICENSE).

---

Last reviewed: July 2026.
