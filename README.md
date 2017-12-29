# Evolving Music Collection Synchronization

This is a process for synchronizing a music collection between two locations using `rsync`.

It is meant to support an evolving file/folder structure, removing files intentionally deleted on the other end.

Must be run on a filesystem that is POSIX compliant.

## Installation

From this path, symlink `emcs` to user's bin directory:

```
if [ ! -d ~/bin ]; then mkdir ~/bin; source ~/.profile; fi
ln -s `pwd`/emcs ~/bin/
```

### Updates

From this path, run:

```
git pull
```

## Usage

```
emcs [label] [location1] [location2]
```

## Process

File deletion runs a simulation first, then asks user permission before actually deleting.

By including `label` as an argument, it supports syncing with other parties, not just two fixed parties.

## License

This code is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
