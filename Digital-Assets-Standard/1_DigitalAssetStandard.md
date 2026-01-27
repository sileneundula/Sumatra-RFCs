# Digital Asset Standard

A Digital Asset is defined by the following:

## Immutable Asset

An Immutable Asset (where bytes are stored on chain)

## Standard Asset

`BLAKE2B_SOURCE_PARSER:` Defines the variable digest length of different content. By default, `SUMIC-BLAKE2-ASSET-STANDARD (SBAS)` is used.

`Required Metadata:` Defines a struct for required metadata for the asset

`Interoperability:` Defines its interoperability with other systems

`Extensions::All:` Defines extensions to the standard

`Nonce:` Defines a nonce that can be used to identify your unique asset.

### SUMIC-BLAKE2-ASSET-STANDARD

`32:` Any Media (offers default security)
`33:` Text
`34:` Image
`35:` Video
`36:` Music
`37:` <NOT TAKEN\>
`38:` <NOT TAKEN\>
`39:` <NOT TAKEN\>
`40:` Executable
`48:` Any (offers high security)
`64:` Any (offers higher security)

A Digest Hash of the Data using BLAKE2B with variable digest.
