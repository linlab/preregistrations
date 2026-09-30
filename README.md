# Pre-registrations

Each folder holds the pre-registration record of one study, named by the study's abbreviation.

- `SHA256SUMS-<version>` lists SHA-256 fingerprints of the analysis plan and code, fixed before the analyses they govern.
- `SHA256SUMS-<version>.ots` is an OpenTimestamps proof that the fingerprint file existed when it was stamped (anchored in the Bitcoin blockchain).

The plan and code are added to the folder when the study is submitted or posted as a preprint. To verify, place the released files next to the fingerprint file, keeping the listed paths, and run:

```
shasum -a 256 -c SHA256SUMS-<version>
ots verify SHA256SUMS-<version>.ots
```

`ots` is the OpenTimestamps client (`pip install opentimestamps-client`).
