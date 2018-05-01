A small script to strip Altera/IntelFPGA SignalTap files of their trace
data.  Rather awkwardly, .stp files contain both configuration necessary for
an FPGA compile, and potentially gigabytes of recorded trace data.
This script will remove the trace data without affecting the configuration.

Usage:

Clean a directory:

    strip-signaltap.sh <directory to clean>

Clean the current directory:

    strip-signaltap.sh

Clean all commits in a git repo:

    cd my-git-checkout
    git filter-branch --tree-filter /full/path/to/strip-signaltap.sh

