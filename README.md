# Syllabus

* **Course:** [PHY325](http://amcdawes.com)
* **Instructors:** Dr. Dawes ([dawes@pacificu.edu](mailto:dawes@pacificu.edu))
* Dr. Hall ([hall@pacificu.edu](mailto:hall@pacificu.edu))

* **Need help?**
  * Open an issue ticket for the project's repository
  * Office hours
    * Dawes: tbd
    * Hall: tbd
  * Stop by or email either of us for 1-on-1 help, or to set up a time to meet

## Table of Contents
* [Contents](#contents)
* [Course description](#course-description)
* [Prerequisites](#prerequisites)
* [Course overview](#course-overview)
  * [Due dates](#due-dates)
* [Grading](#grading)
* [Homework/projects](#homeworkprojects)
  * [Project info](#projectinfo)
  * [Requirements](#requirements)
  * [Workflow](#workflow)
  * [Submission](#submission)
* [External links](#external-links)
  * [Required reading](#required-reading)
  * [Beginner materials](#beginner-materials)
  * [Tools](#tools)
  * [GitHub help](#github-help)
  * [Statements on Plagiarism](#statements-on-plagiarism)
  * [License](#license)

## Course description


## Prerequisites

* Basic programming skills in a language like Fortran, C, or C++
* Workshop Physics
*

## Course objectives
You will leave the course able to:
* Use version control in Github and demonstrate an effective code management workflow.
  *
* Evaluate a system to model and select appropriate numerical methods for solution.
  * based on the physics, what is the best model and explain why
* Debug numerical models
  * catch standard problems: loop tests,
* Verify that numerical results are consistent with a physical model
  * Energy conservation, physical bounds, etc.
*

## Course overview (copied from ICCP, modify as needed)

* **Project 0:** Ising model
  * Introduction to Fortran. Investigation of ferromagnetic dependence on temperature. The Metropolis algorithm. Lattices & boundary conditions.
* **Project 1:** Molecular dynamics
  * Numerical integration of the EoM for a model of argon gas. Minimum image criterion and periodic boundary conditions in a continuum. Free energy, pair correlation, and temperature calculations. Data blocking and energy fluctuations.
* **Project 2:** Advanced Monte Carlo
  * Ising model revisit: the Wolff algorithm, critical phenomena, and data
    structures
  * Polymer conformations: the Rosenbluth algorithm(s), convergence, on- and
    off-lattice models
  * Variational Monte Carlo: the He/H2 ground states
* **Project 3:** Students' choice
  * Lattice Boltzmann
  * Tight-binding
  * Percolation
  * DTFD quantum mechanics
  * etc.

### Due dates
| Project                         |      |
|---------------------------------|------|
| Project 0: Ising model          | TBD  |
| Project 1: Molecular Dynamics   | TBD  |
| Project 2: Advanced Monte Carlo | TBD  |
| Project 3: Students' Choice     | TBD  |

## Grading

* Projects & reports – 75%
* "Final" - 25%
  * Students participating in ICCP give a final presentation at the end of their visit to TU Delft
  * Otherwise, students have a one-on-one oral examination during finals week

## Homework/projects

### Project info
* Ising model
  * [Monte Carlo methods I and outline of the Ising model](http://www.pa.msu.edu/~duxbury/courses/phy480/mclecture1.pdf)
  * [Monte Carlo methods II](http://www.pa.msu.edu/~duxbury/courses/phy480/mclecture2.pdf)
* Argon molecular dynamics
  * [Introduction to MD](http://www.pa.msu.edu/~duxbury/courses/phy480/mdlecture1.pdf)
  * [twoparticles.f90](http://www.pa.msu.edu/~duxbury/courses/phy480/twoparticles.f90)
  * [fcc.f90](http://www.pa.msu.edu/~duxbury/courses/phy480/fcc.f90)
  * [jfcc.nb](http://www.pa.msu.edu/~duxbury/courses/phy480/fcc.nb)
  * [mdlecture2.pdf](http://www.pa.msu.edu/~duxbury/courses/phy480/mdlecture2.pdf)
* Advanced Monte Carlo methods
  * [Intro.pdf](http://www.pa.msu.edu/~duxbury/courses/phy480/ICCPProject2.pdf)
  * [Polymer physics and algorithms review](http://www.pa.msu.edu/~duxbury/courses/phy480/BaschnagelReview2004.pdf)
  * [Ising Monte Carlo paper](http://www.pa.msu.edu/~duxbury/courses/phy480/WolffAlg.pdf)
  * [Variational quantum monte carlo notes](http://www.pa.msu.edu/~duxbury/courses/phy480/VarQMC.pdf)
* Extra project resources
  * [Summary.pdf](http://www.pa.msu.edu/~duxbury/courses/phy480/Project3_2013.pdf)
  * [Tight binding info](http://www.pa.msu.edu/~duxbury/courses/phy480/TightBindingProject.pdf)
  * [Quantum spin chains](http://www.pa.msu.edu/~duxbury/courses/phy480/TISpinChain.pdf)
  * [Numerical Schrodinger dynamics](http://www.pa.msu.edu/~duxbury/courses/phy480/SchrodingerDynamics.pdf)
  * [Lattice Boltzmann](http://www.pa.msu.edu/~duxbury/courses/phy480/BGK_handin.PDF)

### Requirements

To submit a completed project, simply issue a [pull request](https://help.github.com/articles/creating-a-pull-request/) on the original repository before the due date. Your branch should contain:

1. The source code you developed to solve the problem in the `src/` directory and,
1. A written report of your findings in the `report/` directory, typeset in LaTeX

Each project repository contains a skeleton LaTeX file for you to fill in with your report. Your report should follow the style of a research paper (abstract, intro,
etc.) and should contain about five or six pages. Please remember to include all figures in your submission branch!

### Workflow

1. To start, [**fork**](https://guides.github.com/activities/forking/) a project repository
1. [**Clone**](http://gitref.org/creating/#clone) the repository to your computer.
1. Modify the files and [**commit**](http://gitref.org/basic/#commit) changes to complete your solution.
1. [**Push**](http://gitref.org/remotes/#push)/sync the changes up to GitHub.
1. [Create a **pull request**](https://help.github.com/articles/creating-a-pull-request) on the original project repository to turn in the assignment. You can continue to submit changes after you create your pull request -- simply commit and push them.

### Submission
Your pull request should contain both your project and LaTeX source code in separate sub directories; e.g.

```
molecular-dynamics/
├── report/
│   ├── figures/
│   │   ├── energy.pdf
│   │   └── pair_corr.pdf
│   └── md_report.tex
└── src/
    ├── Makefile
    ├── molecular_dynamics.f90
    └── parameters.f90
```
Please **do not** include executables or compiled PDFs (however we need the PDFs corresponding to your images to produce your document, so you should absolutely include them!) We will compile both your program and your report on the HPCC, so please test everything there before submitting.

## External links

### Required reading

* [Computational Physics](http://www.amazon.com/Computational-Physics-Jos-Thijssen/dp/0521833469)
* [The ICCP Coding Notes](https://github.com/ICCP/coding-notes/releases/download/v2015.1/coding_notes.pdf)
* [Real Programmers Don't Use Pascal](http://www.pbm.com/~lindahl/real.programmers.html)

### Beginner materials

In case you need a refresher...

* [PHY201 – Introduction to Fortran](http://www.pa.msu.edu/~duxbury/courses/phy201_f06/phy201_home.html)
* [Fortran 90 reference card](http://www.pa.msu.edu/~duxbury/courses/phy480/fortran90_refcard.pdf)
* [Useful Unix commands](http://www.pa.msu.edu/~duxbury/courses/phy201_f06/UnixCommands.htm)
* [Become an SSH ninja](http://www.xensoft.com/content/become-ssh-ninja-ssh-tips-and-tricks)
* [The LaTeX Wikibook](http://en.wikibooks.org/wiki/LaTeX)

### Tools

* sharing code snippets: [gist.github.com](https://gist.github.com/)
* asking questions: [Stack Overflow](http://stackoverflow.com/)

### GitHub help

* Git and GitHub
    * [Official GitHub Help](https://help.github.com/)
    * [Recommended resources](https://help.github.com/articles/what-**are**-other-good-resources-for-learning-git-and-github)
    * Git: The simple guide [(EN)](http://rogerdudler.github.io/git-guide/)/[(NL)](http://rogerdudler.github.io/git-guide/index.nl.html)
* GitHub Pages
    * [Official site](http://pages.github.com/)
    * [Thinkful guide](http://www.thinkful.com/learn/a-guide-to-using-github-pages/)


### Statements on Plagiarism

From MSU's statement on [Academic Integrity](https://www.msu.edu/unit/ombud/academic-integrity/plagiarism-policy.html):

>Plagiarism (from the Latin plagiarius, an abductor, and plagiare, to steal) defined by the White House Office of Science and Technology Policy on Misconduct in Research as “ . . . the appropriation of another person’s ideas, processes, results or words without giving appropriate credit.” At MSU, General Student Regulation 1.00 states in part that “no student shall claim or submit the academic work of another as one’s own.” (For the complete regulation, see Protection of Scholarship and Grades.) Plagiarism may be accidental or blatant and there is even self-plagiarism.  However, students are held to the same standards whether or not they knew they were plagiarizing or whether or not they were plagiarizing themselves or someone else.

Of course you're free to collaborate with others while working on your projects--that's the whole point of ICCP, after all--just give credit where credit is due. Please respect the terms of use and/or license of any code you find, and if you implement or duplicate an algorithm or code from elsewhere, credit the original source with an inline comment.

### License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work and all other materials under https://github.com/ICCP are licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a> (where applicable). Adopted from the advanced-js course syllabus found [here](https://github.com/advanced-js/syllabus).
