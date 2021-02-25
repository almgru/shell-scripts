# `run-when-changed.sh`

Simple shell script for running a script when a file in a watched directory is modified.

## Dependencies

- `inotify-tools`

## Usage

`run-when-changed watch=<dir to watch> files=<files in dir> script=<script to run>`

Where `<dir to watch>` is a relative or absolute path to the directory containing the file(s) to watch,
`<files in dir>` is a comma-separated list of paths relative to `<dir to watch>`, and `<script to run>` is the relative or absolute path to an executable.

## Example

`run-when-changed watch=data files=points.txt script=generate-graph.sh`

When `data/points.txt` is written to, `generate-graph.sh` is called with `data/points.txt` as an argument.
