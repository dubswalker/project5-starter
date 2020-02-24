# cs610f2019-project05

This repository contains the starter for project five in Computer Science 610
Spring 2020. The `writing`` directory of this repository contains the Markdown  document
for a project that is designed for use with [GitHub
Classroom](https://classroom.github.com/). To learn more about the course in
which these assignments were completed, please visit the [Computer Science Thesis Spring 2020 Allegheny College GitHub Organization](https://github.com/orgs/allegheny-computer-science-thesis-2019).

## Introduction

This assignment requires a researcher to write a Markdown document, stored in the
file `writing/senior_thesis_status_update.md`, that explains three key aspects of work
that you have completed for your proposed senior thesis research project. First,
you should
write a one-paragraph project summary that explains your research project. Second, in a few sentences, you should describe the work that you have already completed. Third, you
should include a bulleted list of the steps that you must take to complete the project and submit all required deliverables before the deadline.

The researcher is also responsible for writing a one-paragraph reflection, at the end of this Markdown document, that explains the challenges that you faced
and the solutions you developed while working on your thesis project so far.
Finally, this is a Markdown
file that must adhere to the standards described in the [Markdown Syntax
Guide](https://guides.github.com/features/mastering-markdown/). Remember, you
can preview the contents of a committed Markdown file by clicking on the name of
the file in your GitHub repository.

If  your writing meet all of the established
requirements, then you will see a green &#x2714; in the listing of commits in
GitHub. If your submission does not meet the requirements, a red &#x2717; will
appear instead. Your course  instructor will reduce a researcher's grade for
this assignment if the red &#x2717; appears on the last commit in GitHub
immediately before the assignment's due date on March 3, 2020 at 1:30 p.m.

Yet, if the green &#x2714; appears on the last commit in your GitHub
repository, then you satisfied all of the main checks, thereby allowing the
course instructors to further evaluate other aspects of your writing, as described in this assignment sheet.
Unless you provide the course instructors with documentation of the extenuating
circumstances that you are facing, no late work will be considered towards your
grade for this project.

## Learning

If you have not done so already, please read all of the relevant [GitHub
Guides](https://guides.github.com/) that explain how to use many of the features
that GitHub provides. In particular, please make sure that you have read the
following GitHub guides: [Mastering
Markdown](https://guides.github.com/features/mastering-markdown/), [Hello
World](https://guides.github.com/activities/hello-world/), and [Documenting Your
Projects on GitHub](https://guides.github.com/features/wikis/). Each of these
guides will help you to understand how to use both [GitHub](http://github.com) and
[GitHub Classroom](https://classroom.github.com/).

## Travis

This assignment uses [Travis CI](https://travis-ci.com/) to automatically run
the checking programs every time you commit to your GitHub repository. The
checking will start as soon as you have accepted the assignment, thus creating
your own private repository. If
you are using Travis for the first time, you will need to authorize Travis CI to
access the private repositories that you created on GitHub. You will partially
complete this authorization by following intuitive steps in your web browser.
You will also need to type the command `travis login --pro` in your terminal
window when you are in the root of your GitHub repository.

### Docker and GatorGrader

The checking programs are a part of the [GatorGrader
tool](https://github.com/GatorEducator/gatorgrader) that allows the users to
automatically verify the satisfaction of the requirements of the submission.
To use this tool, if you have GatorGrader and the appropriate libraries it uses installed locally,
you can run the following command in the terminal:
`gradle grade`

Otherwise, you may use  [Docker
Desktop](https://www.docker.com/products/docker-desktop) to run
following `docker run` command to start `gradle grade` as a containerized
application, using the [DockaGator](https://github.com/GatorEducator/dockagator)
Docker image available on
[DockerHub](https://cloud.docker.com/u/gatoreducator/repository/docker/gatoreducator/dockagator).

```bash
docker run --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator
```

This command will use `"$(pwd)"` (i.e., the current directory) as
the project directory and `"$HOME/.dockagator"` as the cached GatorGrader
directory. Please note that both of these directories must exist, although only
the project directory must contain something. Generally, the project directory
should contain the source code and technical writing of this assignment, as
provided to a student through GitHub. Additionally, the cache directory should
not contain anything other than directories and programs created by DockaGator,
thus ensuring that they are not otherwise overwritten during the completion of
the assignment. To ensure that the previous command will work correctly, you
should create the cache directory by running the command `mkdir
$HOME/.dockagator`. If the above `docker run` command does not work correctly on
the Windows operating system, you may need to instead run the following command
to work around limitations in the terminal window:

```bash
docker run --rm --name dockagator \
  -v "$(pwd):/project" \
  -v "$HOME/.dockagator:/root/.local/share" \
  gatoreducator/dockagator
```

Since the above `docker run` command uses a Docker images that, by default, runs
`gradle grade` and then exits the Docker container, you may want to instead run
the following command so that you enter an "interactive terminal" that will
allow you to repeatedly run commands within the Docker container.

```bash
docker run -it --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator /bin/bash
```

Once you have typed this command, you can use the [GatorGrader
tool](https://github.com/GatorEducator/gatorgrader) in the Docker container by
typing the command `gradle grade` in your terminal. Running this command will
produce a lot of output that you should carefully inspect. If GatorGrader's
output shows that there are no mistakes in the assignment, then your
writing are passing all of the automated baseline checks. However, if the
output indicates that there are mistakes, then you will need to understand what
they are and then try to fix them.

Here are some additional commands that you may need to run when using Docker:

* `docker info`: display information about how Docker runs on your workstation
* `docker images`: show the Docker images installed on your workstation
* `docker container list`: list the active images running on your workstation
* `docker system prune`: remove many types of "dangling" components from your workstation
* `docker image prune`: remove all "dangling" docker images from your workstation
* `docker container prune`: remove all stopped docker containers from your workstation
* `docker container stop ID`: stop the running container with specified ID
* `docker rmi $(docker images -q) --force`: remove all docker images from your workstation

## Problems

If you have found a problem with this assignment's provided source code, then
you can go to the [Computer Science 610 Project 5
Starter](https://github.com/allegheny-computer-science-thesis-2019/project5-starter)
repository and create an issue by clicking the "Issues" tab and then clicking
the green "New Issue" button. To ensure that your issue is properly resolved,
please provide as many details as is possible about the problem that you
experienced.


## Assistance

If you are having trouble completing any part of this project, then please talk
with your first reader. Alternatively, you may ask questions in the Slack
team for this course.
