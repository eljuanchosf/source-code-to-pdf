# source-code-to-pdf

## Origins

This useful utility was born out of the necessity of putting the source code of a friend's app into a PDF.
I couldn't find anything ready to use, so I crafted this horrible, big BASH script. :)

## How to use

**WARNING**: tested ONLY in Ubuntu 14.04

```
cd to-your-awesome-project-root
wget
chmod +x src2pdf
vim src2pdf
# Edit the variables in the top of the file
./src2pdf my_source_code
```

The output file will be `my_source_code.pdf`, but also the *LaTeX* file will be left in case you want to use it.
