# JSCS
## Formatting Validation & Auto-formatting

_Note: regardless of which file you use, be sure to rename it to `.jscsrc` when adding it to your project._

## Usage

Its best to run JSCS in the context of your project so any plugins you add will be available to all users of the project (As opposed to running jscs globally). Use either a gulp task or local npm bin to run jscs:

```bash
npm install jscs --save-dev

# Check files
$(npm bin)/jscs path/to/files

# Check and Auto-format files
$(npm bin)/jscs -x path/to/files
```

## Configuration

While the rules should not be edited except as provided below, you may want to edit the `excludedFiles` in the configuration to weed out files containing library code or anything else you don't want to format.

## File Variations

### [`normal.jscsrc`](normal.jscsrc)

Contains our basic set of rules

### [`es6.jscsrc`](es6.jscsrc)

This file is the same as the normal one, but with an additional flag at the top

### [`jsx.jscsrc`](jsx.jscsrc)

For this configuration, be sure to run the following before usage:

```bash
npm install esprima-fb jscs-jsx-rules --save-dev
```

