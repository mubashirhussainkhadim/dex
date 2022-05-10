Truffle Commands¶
This section will describe every command available in the Truffle application.

Usage¶
All commands are in the following form:


truffle <command> [options]
Passing no arguments is equivalent to truffle help, which will display a list of all commands and then exit.

Available commands¶
build¶
Execute build pipeline (if configuration present).


truffle build
Requires the build key to be present in the configuration. See the Build processes sections for more details.

Warning: The build command and this approach is being deprecated. Please use third-party build tools like webpack or grunt, or see our Truffle Boxes for an example.

compile¶
Compile contract source files.


truffle compile [--list <filter>] [--all] [--network <name>] [--quiet]
This will only compile contracts that have changed since the last compile, unless otherwise specified.

Options:

--list <filter>: List all recent stable releases from solc-bin. If filter is specified then it will display only that type of release or docker tags. The filter parameter must be one of the following: pre-releases, releases, latestRelease or docker.
--all: Compile all contracts instead of only the contracts changed since last compile.
--network <name>: Specify the network to use, saving artifacts specific to that network. Network name must exist in the configuration.
--quiet: Suppress all compilation output.
config¶
Displays and sets user-level configuration options.


truffle config [--enable-analytics|--disable-analytics] [[<get|set> <key>] [<list>] [<value-for-set>]]
Options:

--enable-analytics|--disable-analytics: Enable or disable analytics.
get: Get a Truffle configuration option value.
set: Set a Truffle configuration option value.
list: List all Truffle configuration option values.
console¶
Run a console with contract abstractions and commands available.


truffle console [--network <name>] [--verbose-rpc]
Spawns an interface to interact with contracts via the command line. Additionally, many Truffle commands are available within the console (without the truffle prefix).

Requires an external Ethereum client, such as Ganache or geth. For a console that creates a development and test environment, use truffle develop.

See the Using Truffle Develop and the Console section for more details.

Options:

--network <name>: Specify the network to use. Network name must exist in the configuration.
--verbose-rpc: Log communication between Truffle and the Ethereum client.
create¶
Helper to create new contracts, migrations and tests.
