# Sample Java Project

This is a reference for setting up a new Ant-based Java project. It
contains most of the little Ant tricks I've learned over the
years. When I start a new Java project I clone this repository, remove
sections of build.xml that I don't care about for that particular
project, set the project properties, clear out the sample sources, and
get to work.

## Setup

Building this project requires that Ivy be available to Ant. All you
need is ivy.jar in Ant's classpath (in your `$CLASSPATH`,
`$ANT_HOME/lib`, or `~/.ant/lib`).

## Dependencies

You will need to have Astyle installed and in your path for the
"format" target to work. If it's missing, that's fine. It won't affect
any other targets.

There is a "hotswap" target for replacing live code while an
application is running. You'll need the hotswap Ant extension
installed to use it. This target is to be used alongside the
"run-hotswap" target, which enables hotswapping in the JVM. You can
demo this for yourself by running "run-hotswap" in a terminal, editing
the printed string in the code, and running "hotswap" in another
terminal. The printed message in the running program should change to
the new string.

## Bundles

Take note of the sample `pom.xml` file. This is not actually for Maven
builds -- this is an Ant project afterall -- but for publishing builds
for a Maven repository. It's packed up by the "bundle" target, which
creates a `bundle.jar` containing your project's signed artifacts. To
use the "bundle" target you need to have GnuPG set up in your path, a
generated key pair, and a running `gpg-agent`, unless you like typing
your passphrase a bunch of times in a row.

## Philosophy

I hate coding absolute paths in my build script and I hate including
built files as part of the base project. My philosophy is that the
_environment_ should be set up so that the tool can easily find the
external resources they need (JUnit, etc.) from the system or
dependency manager. It's the system or dependency manager that
provides the libraries. Anyone who has the proper development
environment set up -- one that works across many projects -- should be
able to clone the repository and do a build simply by running the
build program with no special arguments. There should be no need to
edit or install anything into the project space for the initial build.

# This is the change which is updated twice..

`branch1 is created`
$ git --version

# clone repo

git clone https://github.com/aloki9singh/sample-java-project.git

# move to that directory

cd sample-java-project

# list all folders

ls

# list all folders including hidden files

ls --al

# status of staged commit and modified

git status

# staged

git add .

# commit files

$ git commit -m"commit 1"

# pushed to repo  master

$ git push origin master

# status of staged commit and modified

$ git status

$ git add .

# again commit

$ git commit -m"commit 2"

$ git push origin master

# logs of commit

$ git log

#  last commits one line

$ git log -oneline

#  last five commits one line

$ git log --oneline -n 5

# new branch created name branch1

$ git branch branch1

# checking on branch1

$ git checkout branch1

# again stage

$ git add .

# commit files modified 

$ git commit -m"branch1added"

# pushed to branch

$ git push origin branch1

# merged in forked repo


