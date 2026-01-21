# SIP1: Sumatra Blockchain For Censorship-Resistance, Integrity, and Foundational Support

In this Request For Comment, we start by introducing the bottom layer blockchain that will act as a decentralized source of data. This chain is called the `Sumatra Integrity Chain` or `SUMIC L0`.

## Features

Sumatra-Chain is a blockchain that contains the following information:

## Core

- [X] ALMAC ADDRESSES (48-byte addresses using BLAKE2B derived from Public Key Format)
- [ ] Pivotal Namespaces
  - [ ] TrustNet by 0x20CB
- [X] Related Chain Address (RelatedChainAddr)
  - [ ] OpenChain: OpenChain is the protocol to gather data from multiple chains.
  - [ ] EphermalChainWithConfirmation: An Ephermal Chain is a chain that needs trust that will only last until confirmation of chain state and then is stored.
  - [ ] SpawnedChains: A Spawned Chain is one spawned off of the current chain.
  - [ ] 
- [X] Latest State
  - [X] Latest State Updates
  - [X] Uses Generics 
- [ ] Bootstrap Nodes (using public key)
- [ ] Smart Contracts
  - [ ] Use WASM.

## Mutable Sidechains

- [X] Mutable Side-Chain known as `SumatraMutableInfo (SMI)
  - [ ] Dervies from block address
  - [ ] Creates a temporary block lattice
  - [ ] Mutable information can be appended and a confirmation received at end.

## Security
- [ ] Periodic Update (every 10-20 ALMAC blocks)
  - [ ] Chained Hash Value
  - [ ] Periodic Block
    - [ ] Includes Chained Hash
    - [ ] Include Hash Address of All Sent
    - [ ] Include Summary since last periodic update (new) (0x20CB::PERIODICSUMMARYALGORITHM)
      - [ ] Gets hash of the piece of the block lattice for storage


## ALMAC ADDRESS

An ALMAC Address is defined as the following:

> A Base58-Encoded Fixedstr of an input `x` that outputs into 48 bytes (384 bits) using the hash function `BLAKE2B`.
>
> The input, `x` is the public key in X59 Format, using the following algorithms: {ShulginSigning, DualFalconSigning}
>
> It is prepended with the following: [ALMAC/ADDR]

## Novel Technique: Periodic Summary Algorithm

Every so number of blocks on the block lattice need to produce a PERIODICSUMMARY, including all data related to previous blocks, summarized and hashed for easy retrieval. It works in Ticks.
