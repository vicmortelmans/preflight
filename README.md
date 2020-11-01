# Converting PDF to PDF/A1 using ghostscript and preflighting using PDFBox

## required tools:

- Apache PDFBox https://pdfbox.apache.org/download.html (the required jar in this repository, but you may want to get a newer version)
- Ghostscript https://github.com/ArtifexSoftware/ghostpdl-downloads/releases

Note that I got good results with Ghostscript version 9.52, not with 9.53!

## usage

Check the comments in the bash script `pdftopdfa1`

## inspiring articles:

This answer gave the input for composing a working gs command line, featuring a generic PDFA_def.ps file and ICC file: 
https://stackoverflow.com/a/39420880/591336

This answer explains how to work around compatibility errors, setting -dPDFACompatibilityPolicy=3: https://stackoverflow.com/a/59544580/591336

In my script, I detect the path of the script (because that's where the auxiliary files are located as well), like suggested here: https://www.golinuxcloud.com/get-script-name-get-script-path-shell-script/

In my script I use a relative path for the jar file, maybe only required for CygWin, using realpath like in the comments here: https://stackoverflow.com/a/11963966/591336

