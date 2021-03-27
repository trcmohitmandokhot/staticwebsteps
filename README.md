# staticwebsteps
A concise git based guide for static website development using Jekyll. This repository replicates the Jekyll step-by-step tutorial and provides version controlled source code. 

## Objectives
1. Provide source code at each stage of static site development (with version control), as described in Jekyll tutorial.
2. Identify gaps in knowledge of static website development concepts.

## Navigating the repository
src - All source code for this website lies in the root folder.  
website - A githubpages.io website is built from the root directory. You can view the website [here](https://trcmohitmandokhot.github.io/staticwebsteps/).  
**NOTE** - *Due to the way Githubpages.io operates, the website visible at the above link will be for the latest version of the repository.*  
*Users who wish to view the website for a previous version may "build" and "serve" the specific version from a local clone of the repository of interest.*  
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
| Section | Github Repo Version | Tutorial Step |
|:-:|:-:|:-:|
| 1. Basic website | [5391fcb](https://github.com/trcmohitmandokhot/staticwebsteps/tree/5391fcbe8a0f4e98cc854dff04ce2e2eded32698)  | [01-Init](https://jekyllrb.com/docs/step-by-step/01-setup/) |

## 2. Understand and use Liquid Concepts on Webpage
Liquid - A templating language written in Ruby. Three core concepts, which can be understood as:
a) Objects - Similar to variables
b) Tags - Flow control mechanisms (ifs)
c) Filters - Modify output of objects using some predefined functions

This section has two steps:
1) Add *Front Matter* to files (*.html, *.md) to process Liquid.
2) Use filter to modify object "Hello World!" in `<h1>` of `index.html`. We apply the ` | downcase ` filter to the object and observe output.

**Reference Table**
| Section | Github Repo Version | Tutorial Step |
|:-:|:-:|:-:|
| 2. Use Liquid | [46ec279](https://github.com/trcmohitmandokhot/staticwebsteps/tree/46ec2793bec3dc77a8b70bda735c1db60af8c467)  | [02-liquid](https://jekyllrb.com/docs/step-by-step/02-liquid/)  |

## 3. Use frontmatter
This section has two steps:
1) Define webpage title via front matter in the 'index.html' file.
2) For Jekyll to process front matter define character sequence at the top of the file.

**Reference Table**
| Section | Github Repo Version | Tutorial Step |
|:-:|:-:|:-:|
| 3. Use frontmatter | [32c94c2](https://github.com/trcmohitmandokhot/staticwebsteps/tree/32c94c27be0ffb8aa70c143f975226932030fa15)  | [03-front-matter](https://jekyllrb.com/docs/step-by-step/03-front-matter/)  |

## 4&5. Multi-page navigation
This section has four steps:
1) Create a new page using markdown language "about.md"
2) Create a navigation scheme under _includes folder with navigation.html page. 
3) Add a method to navigate between two pages "index.html" and "about.md" using a jekyll liquid concept as shown below in the _layouts/default.html file: 
```ruby
{%include navigation.html %}
{{ content }}
```
4) Use jekyll's methods to modify and highlight current page in the navigation list

**Reference Table**
| Section | Github Repo Version | Tutorial Step |
|:-:|:-:|:-:|
| 4&5. Multi-page navigation | [c7ffb35](https://github.com/trcmohitmandokhot/staticwebsteps/tree/c7ffb35811276b364f369f996e72be5c39b2bc02)  | [05-includes](https://jekyllrb.com/docs/step-by-step/05-includes/)  |

## 6. Include navigation information from data files
Goal - Reduce code duplication by accessing content information from data files, using native jeyll methods. The "navigation.html" file is used as a sample case to demonstrate this technique.

This section has 2 steps
1) Define links and name of page in YAML format inside a _data/navigation.yml file
2) Access content for _includes/navigation.html file from the _data folder using jekyll's technique. 

**Reference Table**
| Section | Github Repo Version | Tutorial Step |
|:-:|:-:|:-:|
| 6. Data Files | [9a3f54c](https://github.com/trcmohitmandokhot/staticwebsteps/tree/9a3f54c71287ddca9f24b6d4b794a9dbad8e1ed1)  | [06-data-files](https://jekyllrb.com/docs/step-by-step/06-data-files/)  |

## 7. Site's SASS/CSS Assets and Styling 
Goal - Demonstrate Jekyll's methods to modularize and apply styling across multiple pages. Use Sass to develop styles.

This section has 4 steps
1) Define a "current" class, which colors text green under the site's _sass directory in a file named "main.scss"
2) Import the style defined in "main.scss" into Jekyll under the site's assets->css folder. 
3) Update the default layout and provide a link to the stylesheet generated by Jekyll. This is a css file, processed by Jekyll based on information contained in the "*.scss" file defined in Step-2.
3) Apply the style to navigation.html code and remove any references to in-line styling.

On completion of these steps, the navigation feature of the website will color the name of current page green.

**Reference Table**
| Section | Github Repo Version | Tutorial Step |
|:-:|:-:|:-:|
| 7. Assets-Styles | [f4f4b6f](https://github.com/trcmohitmandokhot/staticwebsteps/tree/f4f4b6f7782bca41bd0339996738ce4316b95e2c)  | [07-assets](https://jekyllrb.com/docs/step-by-step/07-assets/)  |

# Appendix
*Consider moving this to its own .md file and provide appropriate link*
## Approach & Rules
1. Each section includes one or more steps. 
2. When changes to the website are made, code is pushed to Github. When code is pushed, the section is also published.  
  - Changes to the website can be visual, functional (adding a button), or method (improvement in method).
3. Readme sections should have a clickable reference to version of repo, which includes a code.
