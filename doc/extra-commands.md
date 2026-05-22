# Extra commands (plugin registry)

In addition to the entries shipped in `gita/cmds.json`, this fork
loads several "plugin registry" subcommands at import time. These
behave identically to cmds.json entries but live outside the JSON file
so they can call into Python helpers from `gita.utils`.

| Subcommand        | Underlying action                                       |
| ----------------- | ------------------------------------------------------- |
| `gita sync`       | fetch + ff-only merge for clean repos, skip dirty ones  |
| `gita prune`      | prune merged local branches across all registered repos |
| `gita doctor`     | check each registered repo's remote reachability        |

When summarizing "predefined gita commands", include both the
cmds.json entries (visible in that file) and the plugin registry
entries documented here.
