# Sumatra Improvement Protocol #2: Account Ledger Manager For Long-Term Use And Spawning Side Chains

## 1. Account Ledger Manager (ALMAC)

The Account Ledger Manager (ALMAC) is used as a block lattice to construct differet `synthchains`. These chains all have unique properties, and can be bridged.

### What It Contains

#### ALMAC BLOCK

```rust
use fixedstr::str128;

/// # Almac Block
pub struct AlmacBlock {
    // Contents + Nonce + ChainedHash (All Get Hashed and Signed)
    pub contents: AlmacBlockContents,
    pub nonce: AlmacBlockNonce,
    pub chainedhash: str128,

    // Customizable Container
    pub tx_container_type: AlmacTxType,
    pub tx_action: AlmacAction,
    pub tx_container: String, // Serialize to JSON

    pub synthblockid: u32, // synthblockid

    // Pivot
    pub footer: AlmacBlockFooter,
    pub derivedaddress: str128, // Hash Signature + Footer

    

    //talkaddr: AlmacBlockTalkAddress,

    pub addressing: Option<AddressingContents>,
}
```
### AlmacBlockContents: The Core Content of the Block
```rust
pub struct AlmacBlockContents {
    pub id: BlockID, // BlockID (u64)
    pub ba: BorneoAccount, // BorneoAccount (address)
    pub pk: BorneoPublicKey, // Public Key
    
    pub entry_link_block: Option<BorneoLinkBlock>,
    pub link_hash: BorneoBlockHash,
    
    pub to: BorneoAccount,
    pub from: BorneoAccount,
    
    // ALMAC
    pub almac_version: AlmacVersion,
    pub almac_definitive_type: AlmacDefinitiveType,
    
    pub almac_tx: AlmacTxType,
    pub almac_action: Option<AlmacAction>,
    pub tx_data: String,
}
```
.rs
