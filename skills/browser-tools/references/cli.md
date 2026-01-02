# browser-tools CLI reference

Generated from `./browser-tools.ts --help` and subcommand `--help` output.

Run from:

```sh
cd /Users/rolandk/Sandbox/agent-scripts/scripts/browser-tools
```

## Global

```text
Usage: browser-tools [options] [command]

Lightweight Chrome DevTools helpers (no MCP required).

Options:
  -h, --help                   display help for command

Commands:
  console [options]            Capture and display console logs from the active
                               tab.
  content [options] <url>      Extract readable content from a URL as
                               markdown-like text.
  cookies [options]            Dump cookies from the active tab as JSON.
  eval [options] <code...>     Evaluate JavaScript in the active page context.
  help [command]               display help for command
  inspect [options]            List Chrome processes launched with
                               --remote-debugging-port and show their open tabs.
  kill [options]               Terminate Chrome instances that have DevTools
                               ports open.
  nav [options] <url>          Navigate the current tab or open a new tab.
  pick [options] <message...>  Interactive DOM picker that prints metadata for
                               clicked elements.
  screenshot [options]         Capture the current viewport and print the temp
                               PNG path.
  search [options] <query...>  Google search with optional readable content
                               extraction.
  start [options]              Launch Chrome with remote debugging enabled.
```

## start

```text
Usage: browser-tools start [options]

Launch Chrome with remote debugging enabled.

Options:
  -p, --port <number>   Remote debugging port (default: 9222) (default: 9222)
  --profile             Copy your default Chrome profile before launch.
                        (default: false)
  --profile-dir <path>  Directory for the temporary Chrome profile. (default:
                        "/Users/rolandk/.cache/scraping")
  --chrome-path <path>  Path to the Chrome binary. (default:
                        "/Applications/Google Chrome.app/Contents/MacOS/Google
                        Chrome")
  --kill-existing       Stop any running Google Chrome before launch (default:
                        false). (default: false)
  -h, --help            display help for command
```

## nav

```text
Usage: browser-tools nav [options] <url>

Navigate the current tab or open a new tab.

Options:
  --port <number>  Debugger port (default: 9222) (default: 9222)
  --new            Open in a new tab. (default: false)
  -h, --help       display help for command
```

## console

```text
Usage: browser-tools console [options]

Capture and display console logs from the active tab.

Options:
  --port <number>      Debugger port (default: 9222) (default: 9222)
  --types <list>       Comma-separated log types to show (e.g., log,error,warn).
                       Default: all types
  --follow             Continuous monitoring mode (like tail -f) (default:
                       false)
  --timeout <seconds>  Capture duration in seconds (default: 5 for one-shot,
                       infinite for --follow)
  --color              Force color output
  --no-color           Disable color output
  --no-serialize       Disable object serialization (show raw text only)
  -h, --help           display help for command
```

## pick

```text
Usage: browser-tools pick [options] <message...>

Interactive DOM picker that prints metadata for clicked elements.

Options:
  --port <number>  Debugger port (default: 9222) (default: 9222)
  -h, --help       display help for command
```

## eval

```text
Usage: browser-tools eval [options] <code...>

Evaluate JavaScript in the active page context.

Options:
  --port <number>  Debugger port (default: 9222) (default: 9222)
  --pretty-print   Format array/object results with indentation. (default:
                   false)
  -h, --help       display help for command
```

## cookies

```text
Usage: browser-tools cookies [options]

Dump cookies from the active tab as JSON.

Options:
  --port <number>  Debugger port (default: 9222) (default: 9222)
  -h, --help       display help for command
```

## screenshot

```text
Usage: browser-tools screenshot [options]

Capture the current viewport and print the temp PNG path.

Options:
  --port <number>  Debugger port (default: 9222) (default: 9222)
  -h, --help       display help for command
```

## content

```text
Usage: browser-tools content [options] <url>

Extract readable content from a URL as markdown-like text.

Options:
  --port <number>      Debugger port (default: 9222) (default: 9222)
  --timeout <seconds>  Navigation timeout in seconds (default: 10). (default:
                       10)
  -h, --help           display help for command
```

## search

```text
Usage: browser-tools search [options] <query...>

Google search with optional readable content extraction.

Options:
  --port <number>       Debugger port (default: 9222) (default: 9222)
  -n, --count <number>  Number of results to return (default: 5, max: 50)
                        (default: 5)
  --content             Fetch readable content for each result (slower).
                        (default: false)
  --timeout <seconds>   Per-navigation timeout in seconds (default: 10).
                        (default: 10)
  -h, --help            display help for command
```

## inspect

```text
Usage: browser-tools inspect [options]

List Chrome processes launched with --remote-debugging-port and show their open
tabs.

Options:
  --ports <list>  Comma-separated list of ports to include.
  --pids <list>   Comma-separated list of PIDs to include.
  --json          Emit machine-readable JSON output. (default: false)
  -h, --help      display help for command
```

## kill

```text
Usage: browser-tools kill [options]

Terminate Chrome instances that have DevTools ports open.

Options:
  --ports <list>  Comma-separated list of ports to target.
  --pids <list>   Comma-separated list of PIDs to target.
  --all           Kill every matching Chrome instance. (default: false)
  --force         Skip the confirmation prompt. (default: false)
  -h, --help      display help for command
```

