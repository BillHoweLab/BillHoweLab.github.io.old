# al-folio
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[maintainers]: https://img.shields.io/badge/maintainers-4-success.svg 'Number of maintainers'
<!-- ALL-CONTRIBUTORS-BADGE:END -->

## Template source

This website is a modification of [alshedivat/al-folio](https://github.com/alshedivat/al-folio) under the MIT license.

## Setup and contribution instructions

### Local setup using Docker (Recommended)
Using Docker to install Jekyll and Ruby dependencies is the easiest way.

You need to take the following steps to get the website up and running on your local machine:

- Install [Docker Desktop](https://docs.docker.com/get-docker/). As of Sept 2023, Docker Compose is automatically installed with Docker Desktop, but if not on your machine, install [docker-compose](https://docs.docker.com/compose/install/).
- Run the following command that will pull the latest pre-built image from DockerHub and will run your website.

```bash
$ docker-compose up
```
Note that when you run it for the first time, it will download a docker image of size 400MB or so. 

After you are done editing, you can use the same command (`docker-compose up`) to render the webpage with all you changes. Also, make sure to commit your final changes.

> To change port number, you can edit `docker-compose.yml` file.

To build a custom Docker image (only necessary if you would like to build an older or very custom version), use:

```bash
$ docker-compose -f docker-local.yml up
```

> If you want to update jekyll, install new ruby packages, etc., all you have to do is build the image again using `--force-recreate` argument at the end of previous command! It will download ruby and jekyll and install all ruby packages again from scratch.


### Local Setup (Legacy)

Assuming you have [Ruby](https://www.ruby-lang.org/en/downloads/) and [Bundler](https://bundler.io/) installed on your system (*hint: for ease of managing ruby gems, consider using [rbenv](https://github.com/rbenv/rbenv)*), and also [Python](https://www.python.org/) and [pip](https://pypi.org/project/pip/) (*hint: for ease of managing python packages, consider using a virtual environment, like [venv](https://docs.python.org/pt-br/3/library/venv.html) or [conda](https://docs.conda.io/en/latest/). If you will use only `jupyter`, you can use [pipx](https://pypa.github.io/pipx/)*).

```bash
$ bundle install
# assuming pip is your Python package manager
$ pip install jupyter
$ bundle exec jekyll serve --lsi
```

Now, feel free to customize the theme however you like (don't forget to change the name!).
After you are done, **commit** your final changes.
