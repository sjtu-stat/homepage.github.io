# Lab of Computational Neuroscience @SJTU

[![GitHub contributors](https://img.shields.io/github/contributors/LCNS-SJTU/lcns-sjtu.github.io.svg)](https://github.com/LCNS-SJTU/lcns-sjtu.github.io/graphs/contributors/)
![GitHub](https://img.shields.io/github/license/LCNS-SJTU/lcns-sjtu.github.io?color=blue)
[![GitHub stars](https://img.shields.io/github/stars/LCNS-SJTU/lcns-sjtu.github.io)](https://github.com/LCNS-SJTU/lcns-sjtu.github.io)
[![GitHub forks](https://img.shields.io/github/forks/LCNS-SJTU/lcns-sjtu.github.io)](https://github.com/LCNS-SJTU/lcns-sjtu.github.io/fork)

Website is powered by [Jekyll](https://jekyllrb.com/) with [al-folio](https://github.com/alshedivat/al-folio) theme.

## Getting started

### Local setup
Want to learn more about Jekyll? Check out [this tutorial](https://www.taniarascia.com/make-a-static-website-with-jekyll/).
Why Jekyll? Read [Andrej Karpathy's blog post](https://karpathy.github.io/2014/07/01/switching-to-jekyll/)!


### Installation

For a hands-on walkthrough of al-folio installation, check out [this cool video tutorial](https://www.youtube.com/watch?v=g6AJ9qPPoyc) by one of the community members! 🎬 🍿

---

#### Local setup using Docker (Recommended on Windows)

You need to take the following steps to get `al-folio` up and running in your local machine:

- First, [install docker](https://docs.docker.com/get-docker/)
- Then, clone this repository to your machine:

```bash
$ git clone git@github.com:<your-username>/<your-repo-name>.git
$ cd <your-repo-name>
```

Finally, run the following command that will pull a pre-built image from DockerHub and will run your website.

```bash
$ ./bin/dockerhub_run.sh
```

Note that when you run it for the first time, it will download a docker image of size 300MB or so.

Now, feel free to customize the theme however you like (don't forget to change the name!). After you are done, you can use the same command (`bin/dockerhub_run.sh`) to render the webpage with all you changes. Also, make sure to commit your final changes.

<details><summary>(click to expand) <strong>Build your own docker image (more advanced):</strong></summary>

> Note: this approach is only necessary if you would like to build an older or very custom version of al-folio.

First, download the necessary modules and install them into a docker image called `al-folio:Dockerfile` (this command will build an image which is used to run your website afterwards. Note that you only need to do this step once. After you have the image, you no longer need to do this anymore):
  

```bash
$ ./bin/docker_build_image.sh  
```

Run the website!

```bash
$ ./bin/docker_run.sh
```

> To change port number, you can edit `docker_run.sh` file.

> If you want to update jekyll, install new ruby packages, etc., all you have to do is build the image again using `docker_build_image.sh`! It will download ruby and jekyll and install all ruby packages again from scratch.

</details>

---

#### Local Setup (Standard)

Assuming you have [Ruby](https://www.ruby-lang.org/en/downloads/) and [Bundler](https://bundler.io/) installed on your system (*hint: for ease of managing ruby gems, consider using [rbenv](https://github.com/rbenv/rbenv)*), first [fork](https://guides.github.com/activities/forking/) the repo from `github.com:LCNS-SJTU/lcns-sjtu.github.io` to `github.com:<your-username>/<your-repo-name>` and do the following:

```bash
$ git clone git@github.com:<your-username>/<your-repo-name>.git
$ cd <your-repo-name>
$ bundle install
$ bundle exec jekyll serve
```

Now, feel free to change the forked repository however you like. After you are done, **commit** your final changes.

## Quick Guide

### Create a pull request (PR)

Check [docs](docs/pr.md) about PR creation.

### Journal Club

Check [here](docs/journal_club.md) for docs about adding materials for new journal clubs.

### People

Check [here](docs/people.md) for docs about adding new profiles of group members.

### Publications

Check [here](docs/publications.md) for docs about adding new bib items.

---

## TODO

- [x] Add tutorial for openning a pull-request.
- [x] Add profile avatars for rest of group members.
- [ ] Finish the resource page.
- [ ] Create project page.
