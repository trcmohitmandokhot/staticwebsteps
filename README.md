# staticwebsteps
A concise git based guide for static website development using Jekyll. This repository replicates the Jekyll step-by-step tutorial and provides version controlled source code. 

## Objectives
1. Provide source code at each stage of static site development (with version control), as described in Jekyll tutorial.
2. Identify gaps in knowledge of static website development concepts.

## Navigating the repository
src - All source code for this website lies in the root folder.  
website - A githubpages.io website is built from the root directory. You can view the website [here](https://trcmohitmandokhot.github.io/staticwebsteps/).  
README.md - The documentation for this repository.  
_sites - Jekyll build generated folder (can be safely ignored). Care will be taken to remove it from the repo, to help lower the size and reduce code duplication.

## 0. Installations and Prep
The Jekyll step-by-step [tutorial](https://jekyllrb.com/docs/installation/) is a great reference for installations you need.
On a Linux system, you will need to install the following packages:
1. Ruby
2. Jekyll
3. Bundler

Once these packages (programs?) are installed, the following steps need to be executed (refer to code-blocks on Jekyll webpage).
1. Create a new project directory.
2. Initialize a new Gemfile for the project. A Gemfile captures project's intended dependencies. These are packages (programs? or gems?) used by your project to run your code (website?)
3. Edit the Gemfile and add Jekyll as a new dependency. You may also specify Jekyll version used to build and serve your website. 

**Reference Table**
| Section | Github Repo Version | Comments |
|:-:|:-:|:-:|
| 0 Installations and Prep | [b4997a6](https://github.com/trcmohitmandokhot/staticwebsteps/tree/b4997a6355617643058913496f84df3b244ab0ad)  |   |

## 1. Develop first webpage and "serve"
1. Develop an `index.html` file with **Hello world!** in it. Use a text editor. Place in root of folder. 
2. *Serve* the website: 
  - On a local server using `bundle exec jekyll serve`
  - On github pages, refer to documentation [here](https://docs.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll). To be honest, it should be as easy as having a Gemfile and correct settings for the repository.

**Reference Table**
| Section | Github Repo Version | Comments |
|:-:|:-:|:-:|
| 1. Basic website | [5391fcb](https://github.com/trcmohitmandokhot/staticwebsteps/commit/5391fcbe8a0f4e98cc854dff04ce2e2eded32698)  |   |

# Appendix
*Consider moving this to its own .md file and provide appropriate link*
## Approach & Rules
1. Each section includes one or more steps. 
2. When changes to the website are made, code is pushed to Github. When code is pushed, the section is also published.  
  - Changes to the website can be visual, functional (adding a button), or method (improvement in method).
3. Readme sections should have a clickable reference to version of repo, which includes a code.
