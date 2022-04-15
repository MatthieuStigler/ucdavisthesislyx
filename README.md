# ucdavisthesislyx
This provides a Lyx layout for the [ucdavisthesis TeX package](https://ctan.org/pkg/ucdavisthesis?lang=en). It will enable to run directly the ucdavisthesis package in Lyx. It provides several LyX styles (see left menu) specific to this package, and disables some that are not useful. 

## Installation

1. You need to install the `ucdavisthesis` TeX package, see refereences elsewhere
2. Put the ucdavisthesis.layout in your local lyx layouts folder (Linux: is in home folder ~/.lyx)
3. Do the usual Lyx Tools -> Reconfigure, restart Lyx. 

## Usage

1. Create new document
2. Go to  Documents-> Settings -> Document Class: you should see now *ucdavisthesis* in the document classe menu

## Implementation notes

- The `\authordegrees{}` was intended for adding your degree on main page. I was told by Graduate Studies (2019) this should not be put on that page. Ther problem is that the package expects a degree, or prints a “NO Degree?” warning. I handle this with a \authordegrees{\hfill} (loaded in preamble by lyx layout). This creates a larger space however. Another solution is to use `\authordegrees{}`, will give correct output, but will raise warning.
- I created Lyx style `AbstractThesis`, that creates the environment `abstract`
- I created another Tex environment and Lyx style `AbstractChapter`, meant to be abstract for a specific chapter

## To fix:

- \authordegrees{} should probably be removed (see with package's author)
- Package example contains weird characters...
-  If use same bibliography in multiple files, creates warning in Lyx
