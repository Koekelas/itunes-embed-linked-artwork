# itunes-embed-linked-artwork

iTunes 7 made it possible to download artwork for CDs you've ripped yourself. Artwork downloaded by iTunes is linked to instead of embedded into the tracks. This prevents other programs from displaying the artwork.

itunes-embed-linked-artwork is an iTunes for Windows plugin which searches your entire library for tracks with linked artwork. When it finds such a track, it embeds the linked artwork into the corresponding file.

Note that itunes-embed-linked-artwork is unable to make iTunes download artwork. This is something you'll have to do yourself form inside iTunes prior to launching this script.

# Software requirements

*   Windows Script Host (part of Windows 98 and later);
*   [iTunes][iTunes homepage] 7 or later.

[iTunes homepage]: http://www.apple.com/itunes/ "iTunes Homepage"

# Usage

To run this script, double click it or navigate your shell to it and run:

```
$ embedLinkedArtwork.wsf [options]
```

## Command line options

*   **-h, --help**

    Display help and exit.

*   **-q, --quiet**

    Show less output.

*   **-Q, --quit**

    Quit iTunes when finished.

*   **-v, --verbose**

    Show more output.

*   **-V, --version**

    Display version and exit.

## Examples

```
$ embedLinkedArtwork.wsf --quit
```

Embed linked artwork and quit iTunes when finished.

```
$ cscript //Nologo embedLinkedArtwork.wsf
```

Launch itunes-embed-linked-artwork using cscript, preventing it from spawning a new shell. This is useful if you want the output to be displayed in the current shell instead of a new one. Otherwise, the script behaves the same.

# FAQ

## The message "iTunes is out of sync with reality, skipping track \<trackname>" appears in the output

You'll see this message when you edit your track's metadata with another program then iTunes. Let itunes-embed-linked-artwork finish, make iTunes redownload the artwork and rerun itunes-embed-linked-artwork.

# To-do

*   Allow the user to select a playlist to process.
