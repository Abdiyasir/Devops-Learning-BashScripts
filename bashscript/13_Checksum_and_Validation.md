# Checksum and File Validation in Bash
- Checksums are used to verify the integrity and authenticity of files.
- They generate a unique digital fingerprint for a file — if the file changes, the checksum changes.

## What Is a Checksum?
- A checksum is a hash value calculated from the contents of a file.
- If two checksums match, it confirms that both files are identical and not corrupted.

## Common checksums and how to generate them
- MD5 – widely used, fast, but less secure
- SHA256 – stronger and more reliable
```
md5sum file.txt
sha256sum file.txt
```
- Result: `d41d8cd98f00b204e9800998ecf8427e  file.txt`
