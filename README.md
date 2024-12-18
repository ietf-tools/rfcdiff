# rfcdiff

[rfcdiff web service](https://author-tools.ietf.org/iddiff) | [rfcdiff script](https://github.com/ietf-tools/rfcdiff/raw/main/rfcdiff)

The purpose of this program is to compare two versions of an
internet-draft, and as output produce a diff in one of several
formats:
 * side-by-side html diff
 * paged wdiff output in a text terminal
 * a text file with changebars in the left margin
 * a simple unified diff output

In all cases, internet-draft headers and footers are stripped before generating the diff, to produce a cleaner diff.

## Usage
```
    rfcdiff [options] file1 file2

    rfcdiff takes two RFCs or Internet-Drafts in text form as input, and
    produces output which indicates the differences found in one of various
    forms, controlled by the options listed below. In all cases, page
    headers and page footers are stripped before looking for changes.

    --html      Produce side-by-side .html diff (default)

    --chbars    Produce changebar marked .txt output

    --diff      Produce a regular diff output

    --wdiff     Produce paged wdiff output

    --hwdiff    Produce html-wrapped coloured wdiff output

    --oldcolour COLOURNAME  Colour for new file in hwdiff (default is "green")
    --oldcolor COLORNAME    Color for old file in hwdiff (default is "red")

    --newcolour COLOURNAME  Colour for new file in hwdiff (default is "green")
    --newcolor COLORNAME    Color for new file in hwdiff (default is "green")

    --larger        Make difference text in hwdiff slightly larger

    --browse    Show html output in browser

    --keep      Don't delete temporary workfiles

    --version   Show version

    --help      Show this help

    --info "Synopsis|Usage|Copyright|Description|Log"
            Show various info

    --width N   Set a maximum width of N characters for the
            display of each half of the old/new html diff

    --linenum   Show linenumbers for each line, not only at the
            start of each change section

    --body      Strip document preamble (title, boilerplate and
            table of contents) and postamble (Intellectual
            Property Statement, Disclaimer etc)

    --nostrip   Don't strip headers and footers (or body)

    --ab-diff   Before/After diff, suitable for rfc-editor
    --abdiff

    --stdout    Send output to stdout instead to a file

    --context LINES Provide a different number of lines of context,
            by default 10
```

##  Copyright

```
    Copyright 2002 Henrik Levkowetz
    Copyright 2021 IETF Trust

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program; if not, write to the Free Software
    Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA
```
