Module Session on info theory (`<file>`)
===============================================================================

This is Session on info theory.

The module is part of the [Open Security Education][OpenSecEd] project and the 
maintainer is [Daniel Bosk][Maintainer].  The latest release can be found under 
[releases][Releases].  You can safely link directly to the PDFs found there.

[OpenSecEd]: https://github.com/OpenSecEd
[Maintainer]: https://github.com/Daniel Bosk
[Releases]: https://github.com/OpenSecEd/<file>/releases

This module consists of several learning modules that are linked in this repo.  
However, all required PDFs can be found under [releases][Releases]


Module Overview
===============================================================================

The main document is the study guide, found in the `studyguide/` directory.  
This guide covers the entire course: intended learning outcomes, reading 
instructions with a suggested schedule, assignments and abstracts for the 
material, among other things.

The study guide ties together a set of learning modules.  Each learning module 
contains lectures, assignments etc.  Currently the course comprises the 
following topics:

 - XXX (`XXX`)

These topics are examined using the following assignments.

 - XXX (`XXX`)


File Structure and Building
===============================================================================

*To build* the PDFs, after cloning the repository you must clone its required 
submodules:
```shell
$ git submodule update --recursive --init
```
Then you can go into the directory of the desired document and run `make`.
If you run `make` in the root directory you will recursively transcend the 
directory hierarchy and build everything included in the module.

In each directory the files are structured as follows:

 - contents.tex contains the main contents.
 - aims.tex is an itemized list of the intended learning outcomes, as such it 
   can be included in another document summarizing the list of intended 
   learning outcomes. E.g.
   ```LaTeX
   \begin{itemize}
     \input{aims.tex}
   \end{itemize}
   ```
 - abstract.tex is an abstract of the lecture, assignment, or similar, and 
   covers the required reading instructions, thus you can include these in 
   a study guide containing all reading instructions for the course. E.g.
   ```LaTeX
   \begin{abstract}
     \input{abstract.tex}
   \end{abstract}
 - session.bib contains the bibliography entries, thus this file can be 
 included along with the reading instructions.

