# ReMarkable-sync
Synchronization script for the reMarkable e-reader

Synchronization script for the reMarkable e-reader. The idea is to have a "Library" folder on your PC which is synchronized with the reMarkable. When new files appear in this local directory this script will push them over to the rM. When files are edited, created or annotated on the rM they get converted to .pdf (from .lines) and copied back to the Library folder (with the suffix ".annot").
Nootebooks are also converted to .pdf (with the suffix ".notes").
The folder structure of the "Library" is preserved when syncing with the reMarkable and viceversa.

This project is and adaped version of the work of lschwetlick (https://github.com/lschwetlick/rMsync)
This repository is includes the script https://github.com/lschwetlick/maxio/tree/master/tools, to ensure using the lastet version check if a new version is available.

### Example
- mybook.annot.pdf (annotated file)
- mybook.pdf (original file)
- mynotebook.notes.pdf (written notes)

## Requirements
- imagemagick
- pdftk

You must adjust the paths at the top of the script to your setup before running!

## Usage
usage: sync.py [-b] [-c] [-u] [-d] [-l]

```
optional arguments:
  -b, --backup                        download files from the connected rM
  -c, --convert                       convert the backeup lines files to annotated pdfs and notes
  -u, --upload                        upload new files from the library directory to the rM
  -d, --dry_upload                    runs upload function but without actually pushing anything (just for debugging)
  -l, --makeList                      lists files in the backup directory in plain text (as opposed to hashed)
```
