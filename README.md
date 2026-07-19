# AEGISROM

Public update and runtime feeds for the AEGISDroid Android 13 build for Samsung
Galaxy S9 (`starlte`). Large flashable ZIP files are published as GitHub Release
assets, not committed to this repository.

## Layout

- `builds/starlte.json`: OTA metadata consumed by the system updater.
- `feeds/license.json`: non-device-specific framework license response.
- `feeds/safetyfing.txt`: GMS property feed in the ROM's existing format.
- `feeds/gms_certified_props.json`: compatibility cache used by the legacy
  Clover service.
- `feeds/keyb01x.txt`: encrypted compatibility blob mirrored byte-for-byte from
  the public upstream feed. No decrypted XML or private-key material is stored
  in this repository.

## Security

Never commit bot tokens, GitHub tokens, device serials, IMEI/IMSI values,
subscriber data, proxy credentials, decoded profiles, or decrypted keybox XML.
The runtime currently consumes raw GitHub content, so changes to feed files are
privileged release changes and must be reviewed before merging.

The shared attestation feed can be revoked or rejected and must not be relied on
for important accounts. Replace it only with material you are authorized to use.

