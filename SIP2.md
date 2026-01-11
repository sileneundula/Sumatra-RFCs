# Sumatra Improvement Protocol #2: Account Ledger Manager For Long-Term Use And Spawning Side Chains

## 1. Account Ledger Manager (ALMAC)

The Account Ledger Manager (ALMAC) is used as a block lattice to construct differet `synthchains`. These chains all have unique properties, and can be bridged.

### What It Contains

#### ALMAC BLOCK

```rust
use fixedstr::str128

pub struct AlmacAddress(str128);
pub struct AlmacBlock
```
.rs
