# Introduction

This script was originally written as an exercise in Ruby, to create a
slightly complex script. Its purpose was to monitor RSS feeds on [eztv.it](http://eztv.it) for Torrent links
to new episodes of TV shows. (The website may no longer be available, at least not in its original form.)

# Usage

The recommended use of this script is to call it periodically, ideally from a cron job. You can define your shows in a configuration file (default: `~/.ezrssshows`); whenever the script runs, it checks if new episodes are available. It maintains a datafile (default: `episodes.txt`) to keep track of which episodes have already been downloaded.

The TV shows to monitor are defined in the file `~/.ezrssshows`. This file must be valid Ruby code and define a list that can be traversed with `each`. Each item of the list must be a hash with keys `:name` and `:quality`. These attributes are used to create the RSS search feed.

_Warning:_ No security checking is done on the `.ezrssshows` file; it could be used by an attacker to inject malicious code. Be sure to keep it in a private location.

Syntax:

    ezrss <options>

For help:

    ezrss -h

Unfortunately, a more detailed usage description is not yet available. Look into the script if you are curious.

# Dependencies

The script requires the `lockfile` library from https://github.com/infogrind/rubylibs. All other dependencies are standard Ruby technologies.

# Disclaimer

- The script was developed previous to Ruby 1.9 and has not been tested with
  newer Ruby versions.
- This is for illustration purposes only. Be aware of your local copyright laws
  before downloading or sharing any material on the internet.
