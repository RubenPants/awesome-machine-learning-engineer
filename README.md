# Full stack Machine Learning

## Reproducibility

### Package management

Conda tutorial
https://geohackweek.github.io/Introductory/01-conda-tutorial/

Conda package index
https://www.anaconda.org

Conda myths
http://jakevdp.github.io/blog/2016/08/25/conda-myths-and-misconceptions/

Conda in-depth
https://www.slideshare.net/AaronMeurer/conda-a-binary-scipy2014

### Containerization

Docker getting started
https://docs.docker.com/get-started/

Dockerfile best practices
https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

## Software Engineering

### Meta

Semantic Versioning https://semver.org/

### Python

#### Type annotations

Static type checking with mypy http://mypy-lang.org/

Static type checking with pyre https://pyre-check.org/

Leveraging type system to avoid mistakes https://www.beyondthelines.net/programming/leveraging-the-type-system-to-avoid-mistakes/

## Machine Learning

### Sklearn

Estimators, Transformers http://scikit-learn.org/dev/developers/contributing.html#apis-of-scikit-learn-objects

Custom Estimators http://danielhnyk.cz/creating-your-own-estimator-scikit-learn/

Pipelines http://scikit-learn.org/stable/modules/pipeline.html

Pipelines and custom Estimators http://zacstewart.com/2014/08/05/pipelines-of-featureunions-of-pipelines.html

## DevOps

### Shell

ShellHarden & ShellCheck https://github.com/anordal/shellharden/blob/master/how_to_do_things_safely_in_bash.md

### Terraform

Terraform best practices https://github.com/BWITS/terraform-best-practices


## Tanguy Notes for guide-book

### Conda must have

* Install python packages to Conda env
  * ```flake8``` for linting
  * ```pip install pyre-check``` for type-checking

### VScode installation

* install [VScode](https://code.visualstudio.com/)
* install VScode extensions
  * Python
  * markdownlint
  * ```pyre-vscode``` to enable typechecking in workspace with ```.pyre_configuration``` file
  * pyre-vscode
* Set python conda env in VScode
  * go in ```user settings```
  * find ```"python.pythonPath"``` line
  * edit it in user settings to point to good interpreter

### slack

https://radix-ai.slack.com
communication tool to increase internal communications signal to noise ratio.

### Agile

Software development manifesto that basically describes principles for daily roadmap.

Radix.ai uses *scrum* channel, which contains 3 lines:

* job done today:
* job to do tomorrow:
* what is currently blocking:

### Basic project

* yaml install file (don't forget flake8 to be installed)
* .gitignore
