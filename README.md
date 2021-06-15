# Rackspace Cloud Core Infrastructure Services User Guide

[![Netlify Status](https://api.netlify.com/api/v1/badges/97c80656-30c4-432b-a487-2b9b664fbc36/deploy-status)](https://app.netlify.com/sites/docs-core-infra-user-guide/deploys)

## Purpose

This GitHub repository contains the source files for the Rackspace Cloud Core Infrastructure Services User Guide.

## Contributing

Contributions are welcome!

* To suggest changes or report a problem, submit an [issue](https://github.com/rackerlabs/docs-core-infra-user-guide/issues).

* To make changes to a project, create your own fork of the repository. Then, submit a [pull request](https://github.com/rackerlabs/docs-core-infra-user-guide/compare?expand=1) to have your changes reviewed and merged into the master branch as appropriate.

To contribute content, all you need is an editor and a basic understanding of the project layout and [reStructuredText syntax](http://sphinx-doc.org/rest.html).

You can use the GitHub editor or any text editor to work with documentation source files. For quick syntax checking, try the [Online reStructuredText editor](http://rst.ninjs.org/).

**Note**: If you want to build the project, you need to install the [Sphinx documentation generator](http://www.sphinx-doc.org/en/stable/install.html).

## Source format

The Rackspace Cloud Core Infrastructure Services Guide is developed and built using the [Python Sphinx documentation generator](http://sphinx-doc.org/). Content is written in [reStructuredText](http://sphinx-doc.org/rest.html), the markup syntax and parser component of [Python Docutils](http://docutils.sourceforge.net/index.html).

The repository includes the documentation source files, Sphinx configuration and build files, as well as any required Sphinx extensions and build tools.

## Structure

Source files for the Sphinx documentation project are in the main `docs-core-infra-user-guide` directory. Following are the key files that define the Spinx project and content architecture for the documentation:

| Content | File |
|---|---|
| Sphinx documentation configuration file | [conf.py](https://github.com/rackerlabs/docs-core-infra-user-guide/blob/master/conf.py) (Typically, this file does not require changes.) |
| Index page for the main content structure | [index.rst](https://github.com/rackerlabs/docs-core-infra-user-guide/blob/master/index.rst) |
|User Guide introduction index | [cloud-guide-intro/index.rst](https://github.com/rackerlabs/docs-core-infra-user-guide/blob/master/cloud-guide-intro/index.rst) |
| Cloud configuration index | [cloud-config/index.rst](https://github.com/rackerlabs/docs-core-infra-user-guide/blob/master/cloud-config/index.rst) |
| Cloud interfaces index | [cloud-interfaces/index.rst](https://github.com/rackerlabs/docs-core-infra-user-guide/blob/master/cloud-interfaces/index.rst) |
| Introducing the Rackspace cloud | [cloud-intro/index.rst](https://github.com/rackerlabs/docs-core-infra-user-guide/blob/master/cloud-intro/index.rst) |
| Cloud operations index | [cloud-ops/index.rst](https://github.com/rackerlabs/docs-core-infra-user-guide/blob/master/cloud-ops/index.rst) |
| Cloud productivity index | [cloud-preprod/index.rst](https://github.com/rackerlabs/docs-core-infra-user-guide/blob/master/cloud-preprod/index.rst) |
| **make.bat** | Windows build script |
| **Makefile** | Linux and OS X build |

## Support and feedback

If you find a problem, open a GitHub [issue](https://github.com/rackerlabs/docs-core-infra-user-guide/issues).

If you need additional assistance, contact us at <devdoc@rackspace.com>.

## Local Setup

`npm i -g netlify-cli`
`netlify init`
`netlify build`
`netlify dev`
`netlify deploy`
