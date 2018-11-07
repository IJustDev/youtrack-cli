# youtrack-cli
Command Line Tool for interacting with youtrack

[![Build Status](https://travis-ci.com/shanehofstetter/youtrack-cli.svg?branch=master)](https://travis-ci.com/shanehofstetter/youtrack-cli)


## Install
```
npm install -g youtrack-cli
```
```
yarn add youtrack-cli
```


## Usage

After you've installed the package globally, youtrack-cli will be available as `youtrack` in your command line.

### Getting started

To setup the cli (set the URL, provide your credentials), run:
```bash
$ youtrack setup
```
This will guide you through the setup process.

### Commands

```
youtrack -h
```

Available commands are:

```
project|p      manage projects
user|u         manage users
setup          setup youtrack cli
```


#### Projects

```
$ youtrack project <subcommand> <options>
```

Available subcommands:

```
list|ls [options]  list all accessible projects
```


##### list

```
Options:
  -r, --raw   print raw json
  -d, --desc  print description (does not apply when option --raw is used
```

Example:  

```bash
$ youtrack project ls
```

![image](https://user-images.githubusercontent.com/13404717/48026722-28e7af00-e147-11e8-8716-e63e9be1d0f8.png)


#### Users

```
$ youtrack user <subcommand> <options>
```

Available subcommands:

```
info|i [options]        show info about current user
show [options] <login>  show info about user
```


#### Issues

```
$ youtrack issue <subcommand> <options>
```

Available subcommands:

```
find|f [options]            search issues with a query (starts prompt)
show|s [options] <issueId>  show issue info
```

##### find

```
Options:
  -r, --raw             print raw json
  -m, --max <max>       limit number of issues shown
  -f, --fields <field>  which fields to display
```

Example:  

```bash
$ youtrack issue f
```

![image](https://user-images.githubusercontent.com/13404717/48168483-ac440480-e2ef-11e8-9de5-6484deb0bad4.png)

#### Work-Items (Timetracking)

```
$ youtrack workitem <subcommand> <options>
```

Available subcommands:
```
list|ls [options] <issueId>  list all workitems for issue
create|c [options]           create new work item for an issue (opens prompt)
```

##### list

```
Options:
  -r, --raw             print raw json
```

Example:  

```bash
$ youtrack workitem ls T1-2
```

![image](https://user-images.githubusercontent.com/13404717/48168349-232ccd80-e2ef-11e8-9cb7-dbe8222e0203.png)

