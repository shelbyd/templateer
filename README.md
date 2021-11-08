# templateer
Apply template directories/repositories to your local project.

Use a template repository in your project without cluttering source control with the boilerplate.
Incidentally, upgrade boilerplate from the template trivially.

## WIP

This project is currently not implemented and is a work in progress. This documentation is only for reference for how the project will work.

## Installation

Templateer uses Rust. Install at https://rustup.rs/. Then:

```
cargo install templateer
```

## Usage

```
cd project/here
tpl init https://github.com/some/template
# make your changes to template files
tpl genpatch # generate semantic patch files
# commit to VCS
# pull VCS changes
tpl applypatch
```

### Details

Templateer's goal is remove template boilerplate from your project's source control.
It will:

1. Not override checked in conflicting files
2. Merge the contents of directories.
3. Generate easily readable patch files for common configuration formats (JSON, YAML, etc)
4. Generate standard UNIX patch files when it can't generate a more easily readable patch
