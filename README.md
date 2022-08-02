# entrusted-snapshots

Snapshot builds for the [entrusted application](https://github.com/rimerosolutions/entrusted).
This helps asses Windows issues as I sadly don't have a Windows machine (switch to UNIX/Linux 20+ years ago).

## Changelog

### 20220802

- Ensure that the UI is responsive during conversions 
 - Always consume Docker output even if not displayed in sanity checks prior the actual processing
 - This avoids the conversion progress information being stuck at 1%
- Avoid false positives when the conversion actually succeeds: 
  - On Windows changing the file modification date of the resulting PDF file fails and doesn't appear to be required at all
  - The solution is to avoid marking the conversion as failed, if changing the file modification date fails


### 20220801

Snapshot build for command-line error when the OCR language is not set.

### 20220730

Snapshot build for general UI responsiveness issues and Windows specific annoyances
- Avoid displaying a command prompt on Windows while running shell commands
- Prevent the user interface from "freezing" during conversions, via better coding practices
