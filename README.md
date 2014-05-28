Docs: Rackspace Cloud Core Infrastructure Services User Guide
=============================================================

This system uses the Python Sphinx tool for structure & building as part of the
static build process. Included is a Makefile & make.bat file for cross platform
building (for development/contribution).

Layout:

* **_static**: static assets unique to the documentation; this may include js,
  css, images, etc.
* **_templates**: custom html templates
* **conf.py**: Configuration, no touchy.
* **index.rst**: Main index / landing page for the docs
* **make.bat**: windows build script
* **Makefile**: linux/osx build

You will need [Sphinx](http://sphinx-doc.org/) installed to build - however to
contribute, all you need is a basic understanding of the project layout and
Restructured Text. [Here is an excellent ReST primer](http://sphinx-doc.org/rest.html).

Once you're all set up: in order to build run:

```
make html
```

You will see the build output and the static files will be dropped in:

```
_build/html
```

On OS/X you can run:

```
open _build/html/index.html
```

To pop open the doc index and preview.


Adding documentation
--------------------

Here's a brief description of the document writing workflow:

1. Fork and then clone the repo (https://github.com/rackerlabs/docs-core-infra-user-guide)
2. git remote add upstream https://github.com/rackerlabs/docs-core-infra-user-guide.git
3. git pull upstream master
4. Create a git branch named after the topic you are going to write about
5. Follow the basic structure and ReST conventions present in other existing .rst files
6. Run Sphinx (as explained above)
7. If no errors, git commit[1], then git push origin branch-name
8. Submit PR from your branch, to upstream master

[1] We're not committing and pushing the output HTML files. We're only going to commit and push the .rst files. The static pages will then be built, rendered and deployed automatically by the CI.
