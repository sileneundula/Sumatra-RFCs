# SIP1: Sumatra Blockchain For Censorship-Resistance, Integrity, and Foundational Support

In this Request For Comment, we start by introducing the bottom layer blockchain that will act as a decentralized source of data. This chain is called the `Sumatra Chain`.

## Features

Sumatra-Chain is a blockchain that contains the following information:

## Core

- [X] ALMAC ADDRESSES (48-byte addresses using BLAKE2B derived from Public Key Format)
- [X] Latest State
  - [X] Latest State Updates
  - [X] Uses Generics 
- [ ] Bootstrap Nodes (using public key)


## Security
- [ ] Periodic Update (every 10-20 ALMAC blocks)
  - [ ] Chained Hash Value
  - [ ] Periodic Block
    - [ ] Includes Chained Hash
    - [ ] Include Hash Address of All Sent
    - [ ] Include Summary since last periodic update (new) (0x20CB::PERIODICSUMMARYALGORITHM)
      - [ ] Gets hash of the piece of the block lattice for storage
         

## Novel Technique: Periodic Summary Algorithm

Every so number of blocks on the block lattice need to produce a PERIODICSUMMARY, including all data related to previous blocks, summarized and hashed for easy retrieval. It works in Ticks.
