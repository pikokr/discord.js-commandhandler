# typing

## commandHandlerClient
#### extends [discord.js#Client](https://discord.js.org/#/docs/main/stable/class/Client)

### Constructor
```js
new CommandHandlerClient(options)
```

| PARAMETER | TYPE | DESCRIPTION |
|-----------|------|-------------|
| options | <a href='#commandhandlerclientoptions'>commandHandlerClientOptions</a> | commandHandlerClient's Option |

### Properties

#### .prefix
Bot's prefix
> Type: string

> Default: `'!'`

#### .path
command file's path
> Type: string

#### .token
- **The Dangers! This is Your Bot Token.**
> Type: string

### Methods

#### .loadCommandWithFile()
ext: [js, ts]

path: commandHandlerClientOptions.path
> Description: `[path]/<fileName>.[ext] Load`

#### .loadCommandWithFolder()
ext: [js, ts]

path: commandHandlerClientOptions.path
> Description: `[path]/<folderName>/<fileName>.[ext] load`


#### loadSlashGuildCmdWithFile(`clientId`, `guildId`)
| PARAMETER | TYPE | DESCRIPTION |
|-----------|------|-------------|
| clientId | string | bot's ID |
| guildId | string | guild's ID |

ext: [js, ts]

path: commandHandlerClientOptions.path
> Description: `[path]/<fileName>.[ext] slashCommand guild Registry`

#### loadSlashCmdWithFile(`clientId`)
- **this is global slashCommand.**

| PARAMETER | TYPE | DESCRIPTION |
|-----------|------|-------------|
| clientId | string | bot's ID |

ext: [js, ts]

path: commandHandlerClientOptions.path
> Description: `[path]/<fileName>.[ext] slashCommand Registry`

#### loadSlashGuildCmdWithFolder(`clientId`, `guildId`)
| PARAMETER | TYPE | DESCRIPTION |
|-----------|------|-------------|
| clientId | string | bot's ID |
| guildId | string | guild's ID |

ext: [js, ts]

path: commandHandlerClientOptions.path
> Description: `[path]/<folderName>/<fileName>.[ext] slashCommand guild Registry`

#### loadSlashCmdWithFolder(`clientId`)
- **this is global slashCommand.**

| PARAMETER | TYPE | DESCRIPTION |
|-----------|------|-------------|
| clientId | string | bot's ID |

ext: [js, ts]

#### runMessage(`message`, `client`)
| PARAMETER | TYPE | DESCRIPTION |
|-----------|------|-------------|
| message | [discord.js#Message](https://discord.js.org/#/docs/main/stable/class/Message) | discord.js Message |
| client | [commandHandlerClient](#commandhandlerclient) | commandHandlerClient |

> Description: `commandHandler Run`

#### runSlash(`interaction`, `client`)
| PARAMETER | TYPE | DESCRIPTION |
|-----------|------|-------------|
| message | [discord.js#Interaction](https://discord.js.org/#/docs/main/stable/class/Interaction) | discord.js Interaction |
| client | [commandHandlerClient](#commandhandlerclient) | commandHandlerClient |

> Description: `commandHandler Run`

## commandHandlerClientOptions
| PARAMETER | TYPE | DESCRIPTION | DEFAULT | EXAMPLE |
|-----------|------|-------------|---------|---------|
| prefix? | string | command's prefix | `'!' `| `'.'` |
| path | string | command file's path | ***NONE*** | `__dirname + '/commands'` |
| token | string | bot's token | ***NONE*** | ***NONE*** |