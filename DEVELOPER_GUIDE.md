# Developer Guide

This document lays out different standards on our way to develop at MIC's this is not project-specific but rather guidelines for any kind of software development in our company.

## Why we write code

We believe that code must de produced for a very specific goal and not just for the sake of it, in order to preserve its quality. Before thinking about writing a new (very cool) feature, please ask yourself how will it serve the projects but ultimately its users. While it is complicated sometimes to picture that, we strongly encourage you to discuss about your ideas with other contributors before even writing code.  

## Quality of code

### Coding style

Sometimes the community struggles to define strong norms depending on the project's type, the language used or even the framework you are using. That's why we will ask you to just follow the ones we apply to our projects in order to stay consistent. If no norm nor coding style is specified, we would just advise you to follow the most popular one amongst the community of the language you are using (if it makes sens to you, of course) then to write a small paragraph about why you chose it so we can define it as a standard in our project.  
If the language you are using has a style guide, you should follow it. Examples are [PEP8 for python](https://www.python.org/dev/peps/pep-0008/), [Apache's C style guide](https://httpd.apache.org/dev/styleguide.html) or [Google Style Guides](https://google.github.io/styleguide/).  
We also encourage you to use formatter tools such as [black](https://github.com/psf/black) for python, [google-java-format](https://github.com/google/google-java-format) for java or [gnu indent](http://www.gnu.org/software/indent/) for C/C++ code. You can find a non exhaustive list of code formatters here: https://github.com/rishirdua/awesome-code-formatters

### Testing 

Unit tests are strongly recommended in any software development project, it is especially useful for open source or collaborative projects since somebody is most likely going to base their work on yours. Providing tests with your features will help them making sure what they are working on is tested and approved, thus allowing them to focus on their features which ultimately will lead to a gain of time for everyone.  
We are not advising to aim for code coverage but rather to focus on the essentials: do not prove that 2+2 is 4 (quick maths) but rather focus on the dependencies of your method are they all tested? Is your feature tested? What are the use cases? Is there any edge cases that could break your code? Tests are a good way to try to see your code on a user's point of view. While using this approach, it might be useful to look into Test-Driven Development which forces you to shift right away.  
Of course, the methodology is yours and what matters ultimately is that your feature is tested.
