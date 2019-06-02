## pulumi preview

Show a preview of updates to a stack's resources

### Synopsis

Show a preview of updates a stack's resources.

This command displays a preview of the updates to an existing stack whose state is
represented by an existing state file. The new desired state is computed by running
a Pulumi program, and extracting all resource allocations from its resulting object graph.
These allocations are then compared against the existing state to determine what
operations must take place to achieve the desired state. No changes to the stack will
actually take place.

The program to run is loaded from the project in the current directory. Use the `-C` or
`--cwd` flag to use a different directory.

```
pulumi preview [flags]
```

### Options

```
      --analyzer strings         Run one or more analyzers as part of this update
      --config-file string       Use the configuration values in the specified file rather than detecting the file name
  -d, --debug                    Print detailed debugging output during resource operations
      --diff                     Display operation as a rich diff showing the overall change
      --expect-no-changes        Return an error if any changes are proposed by this preview
  -h, --help                     help for preview
  -j, --json                     Serialize the preview diffs, operations, and overall output as JSON
  -m, --message string           Optional message to associate with the preview operation
  -p, --parallel int             Allow P resource operations to run in parallel at once (1 for no parallelism). Defaults to unbounded. (default 2147483647)
      --show-config              Show configuration keys and variables
      --show-replacement-steps   Show detailed resource replacement creates and deletes instead of a single step
      --show-sames               Show resources that needn't be updated because they haven't changed, alongside those that do
  -s, --stack string             The name of the stack to operate on. Defaults to the current stack
      --suppress-outputs         Suppress display of stack outputs (in case they contain sensitive values)
```

### Options inherited from parent commands

```
      --color string                 Colorize output. Choices are: always, never, raw, auto (default "auto")
  -C, --cwd string                   Run pulumi as if it had been started in another directory
      --disable-integrity-checking   Disable integrity checking of checkpoint files
  -e, --emoji                        Enable emojis in the output
      --logflow                      Flow log settings to child processes (like plugins)
      --logtostderr                  Log to stderr instead of to files
      --non-interactive              Disable interactive mode for all commands
      --profiling string             Emit CPU and memory profiles and an execution trace to '[filename].[pid].{cpu,mem,trace}', respectively
      --tracing string               Emit tracing to a Zipkin-compatible tracing endpoint
  -v, --verbose int                  Enable verbose logging (e.g., v=3); anything >3 is very verbose
```

### SEE ALSO

* [pulumi](pulumi.md)	 - Pulumi command line

###### Auto generated by spf13/cobra on 13-May-2019