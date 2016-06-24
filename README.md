# source-code-to-pdf

## Origins

This useful utility was born out of the necessity of putting the source code of a friend's app into a PDF.
I couldn't find anything ready to use, so I crafted this horrible, big BASH script. :)

## How to use

**WARNING**: tested ONLY in Ubuntu 14.04

```
cd to-your-awesome-project-root
wget https://raw.githubusercontent.com/eljuanchosf/source-code-to-pdf/master/src2pdf
chmod +x src2pdf
vim src2pdf
# Edit the variables in the top of the file
./src2pdf my_source_code
```

The output file will be `my_source_code.pdf`, but also the *LaTeX* file will be left in case you want to use it.

### File types

There is one **very important** code block. It is used to specify which files we want to include and what languages are they written:

```sh
# The language    # File pattern # Exclude files
file_types[0]="php|-name '*.php'|! -name '*.blade.php'"
file_types[1]="html|-name '*.blade.php'|"
```

In the example, I go for `php` and `.blade.php` files.
Since Python's *Pygments* doesn't have a *blade* format, I set it as HTML. In this way, Pygments will know what language to use when doing the syntax highlightning.

You can add as many groups as you want. Copy, paste and replace.

Each group's section is sepparated by a pipe (|):
* The first section is the language name according to Pygments specification.
* The second section is a pattern on what files do you want to include.
* The third section is a pattern on what files do you want to *exclude*.

There is nothing more to it... enjoy! (let me know if you use it!)
