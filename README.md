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

### environment.yml skeleton for new projects

```yml
name: "your conda environmnent name"
channels:
 - defaults
 - conda-forge
dependencies:
 - flake8  # linting
  - mypy  # linting and type-checking
 - autopep8  # python code auto-formating
 - pip:
    - pyre-check  # type-checking
# perhaps add the code-complexity package
```

Create the environment by opening a terminal and typing:

```bash
conda env create -f environment.yml
```

### VScode set-up

* install [VScode](https://code.visualstudio.com/)
* install VScode extensions
  * Python
  * markdownlint
  * pyre-vscode
* If conda env not automatically detected, set it manually:
  * go in ```user settings```
  * find ```"python.pythonPath"``` line
  * edit it to point to good python bin
* Minimum user settings

  ```python
  {
    "python.linting.pylintEnabled": false,
    "python.linting.flake8Enabled": true,
    "python.linting.mypyEnabled": true,
    "python.linting.enabled": true,
    "editor.formatOnSave": true,
    "python.formatting.provider": "autopep8",
    "editor.rulers": [
        79
    ]
  }
  ```

### project set-up

A project should contain at least the following files:

* `.gitignore`
* `README.md`

Activate pyre type-checking by opening a terminal in the project-root and type ```pyre init```.

### radix.ai style

* Documentation: google style
* Policy regarding sanity checks: assert vs raise vs type-checking? type checking cannot supplant assert or raise, but can replace trivial types case.

### Slack

Communication tool used by [radix.ai](https://radix-ai.slack.com) to increase internal communications signal to noise ratio.

#### Scrum

On slack, the radix.ai **scrum** channel is inspired by the AGILE Software development manifesto that basically describes principles for daily roadmaps.

At the end of the day, use the *scrum* channel to convey, on 3 lines:

* job done today:
* job to do tomorrow:
* what is currently blocking:

#### Flask

