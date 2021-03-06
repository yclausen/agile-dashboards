Issue Splitter operator
======================

The issue-splitter-operator is a WireCloud operator that provides the ability to split normalized issue data obtained with the agile harvesters.

Build
-----

Be sure to have installed [Node.js](http://node.js) in your system. For example, you can install it on Ubuntu and Debian running the following commands:

```bash
curl -sL https://deb.nodesource.com/setup | sudo bash -
sudo apt-get install nodejs
sudo apt-get install npm
```

If you want the last version of the operator, you should change to the `develop` branch:

```bash
git checkout develop
```

Install other npm dependencies by running: (need root because some libraries use applications, check package.json before to be sure)

```bash
sudo npm install
```

For build the operator you need download grunt:

```bash
sudo npm install -g grunt-cli
```

And now, you can use grunt:

```bash
grunt
```

If everything goes well, you will find a wgt file in the `dist` folder.

## Wiring

### Input Endpoints

-`Issue list`: A normalized issue list. Can be obtained with any agile issue harvester operators.

### Output Endpoints

-`Issue status list`: A list of the statuses the issues had.
-`Issue priority list`: A list of the priorities the issues had.
-`Issue assignee list`: A list of the assignees the issues had.
-`Issue type list`: A list of the types the issues had.

## Usage

Plug in a list of normalized issues, which can be obtained with any agile issue harvester operator, such as the `jira-harvester-operator` and filtered with the `set-generic-filter-conditions` and the `and-filter-operator`.

## Reference

- [FIWARE Mashup](https://mashup.lab.fiware.org/)

## Copyright and License

Copyright (c) 2016 CoNWet
