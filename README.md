# gb

[![wercker status](https://app.wercker.com/status/494a8ac6b836f39cc7e67036d957a43e/m/master "wercker status")](https://app.wercker.com/project/bykey/494a8ac6b836f39cc7e67036d957a43e)

`gb` is a proof of concept replacement build tool for the [Go programming language](https://golang.org).

I gave a talk about `gb` and the rational for its creation at GDG Berlin in April 2015, [video](https://www.youtube.com/watch?v=c3dW80eO88I) and [slides](http://go-talks.appspot.com/github.com/davecheney/presentations/reproducible-builds.slide#1).

## Project based

`gb` operates on the concept of a project. A gb project is a workspace for all the Go code that is required to build your project.

A gb project is a folder on disk that contains a subdirectory named <code>src/</code>. That's it, no environment variables to set. For the rest of this document we'll refer to your <code>gb</code> project as <code>$PROJECT</code>.

You can create as many projects as you like and move between them simply by changing directories.

## Installation

    go get github.com/constabulary/gb/...

## Read more

gb has its own site, [getgb.io](http://getgb.io/), head over there for more information.

## Contributing

### Road map

In rough order

- [Cross Compilation](https://github.com/constabulary/gb/milestones/cross-compilation)
- gb test improvements, test output, flag handling
- gb vendor updates and bug fixes
- new package resolver (replace go/build)

### Big ticket items 

Big ticket items that are not on the road map yet

- [Race detector support](https://github.com/constabulary/gb/issues/96)
- Tag handling, unify -tags, ENVVARS and GOOS/GOARCH into a single format for binary names and pkg cache
- Package BuildID support (make stale detection work like the Go 1.5)
- `gccgo` toolchain support.

We welcome pull requests, bug fixes and issue reports.

Before proposing a large change, please discuss your change by raising an issue.
