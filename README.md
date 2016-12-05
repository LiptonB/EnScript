# EnScript utilities for speeding up investigations

## AddImages.EnScript

This script allows several disk images to be imported at the same time. To use, first open a case and run the AddImages.EnScript script. Select a directory with images to process, then select the checkboxes next to the images you wish to import. Click OK. The images will be added to the case.

The tool accepts two file extensions:
* .img: Imported as a raw, full-disk image
* .E01: Imported as an EnCase evidence file

## CreateHashSet.EnScript

This script will create a list of hashes from the selected files and then extract them so we can compare them with the list of whitelist or blacklist hashes. This script will calculate md5 and sha1 hashes.

## FindPrintJobs.EnScript

This script will iterate all the files inside the evidence and look for the printed job, cached inside the image. Because a user can change the location of spool location we did not limited our search only to that folder but we looked for every file with the spool print extension (SPL).

## MismatchedExtensions.EnScript

This tool iterates through the files in all evidence in the current case, and identifies files which have a file extension that doesn't match the file signature. This can be used to find files that have been  renamed with a different extension to hide their contents. To use the tool, simply open a case and run the MismatchedExtensions.EnScript script. The script will display a window presenting the found files, and also add them to bookmarks within the case.

## ScanRegistry.EnScript

This script will parse the set registry key and look for a value. The ideal use of this script is to have a list of blacklisted softwares to see if those software are installed on the end point or we can have a list of default setting for the endpoint registry to make sure that the used has not change them. 
