# GAH Release Repo

GAH (Google Auth Helper) release-only repository.

- Code repo (private): `https://github.com/greenhelix/GAH-Code-Repo`
- Release repo: `https://github.com/greenhelix/GAH-Release-Repo`

## What Is In This Repo

Only versioned release artifacts are stored here.

```text
releases/
  vX.Y.Z/
    gah-ubuntu-vX.Y.Z.tar.gz
    gah-windows-web-vX.Y.Z.zip
    checksums.txt
```

## Quick Install (Ubuntu)

1. Download latest `gah-ubuntu-vX.Y.Z.tar.gz` from `releases/vX.Y.Z/`
2. Extract:

```bash
sudo mkdir -p /opt/google-auth-helper
sudo tar -xzf gah-ubuntu-vX.Y.Z.tar.gz -C /opt/google-auth-helper
cd /opt/google-auth-helper
```

3. Run installer in the extracted package:

```bash
sudo bash deploy/install.sh
```

## Version History

| Version | Date | Core Changes |
|---|---|---|
| v0.0.0 | 2026-03-06 | Release repo bootstrap (structure + README policy) |

## Notes

- Keep this repo simple: artifacts + checksums + short history.
- Detailed technical docs stay in `GAH-Code-Repo`.
