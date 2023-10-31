# csharp-gamedev-coding-convention
A coding convention based on my personal experiences on what provides the most optimal clarity.

## General rules
- PascalCase for: classes, constants, enums, non-private statics.
- camelCase  for: everything else than what's above.
- Never use CAPS.
- Avoid magic numbers. (todo: elaborate and/or add examples)
- When declaring things at class-scope & if lines are not separated by a blank row: Align the indentation of keywords, types, assignments, semicolons. (picture example: TODO)
- Local variable names can be abbreviated only if the context to understand the abbreviation from is within same scope.
- Prefix private class members with an underscore '_'
- Try to section properties wherever possible (by sectioning I mean, separate a wall of rows into sensible groups of rows using line breaks (see example: TODO).

## Examples
### Naming conventions
TODO (for now, see general rules)

### Indentation
TODO: add a write up of indentation rules right here.

Note: I acknowledge these recommendations may come off as cursed, but see the difference and judge for yourself.

```csharp
// Good - clean, easy to read, uniform.
const string ToggleAction        = "ToggleConsole"; // Align everything according to the longest line in a section
const string SendLineAction      = "SendLine"     ;
const string SpectateLeftAction  = "SpectateLeft" ;
const string SpectateRightAction = "SpectateRight";

public const string ConsoleGroup  = "gd-console" ;
public const string SpectateGroup = "CanSpectate";

const string ImaginaryVariable = "1"; // This is a section that contains a single line, hence it's aligned "normally" so to speak, without regard to what's above or below.

private static bool        _isSpectating = false;
private static Array<Node> _spectateList        ;
private static int         _activeSpectateIdx   ;

public static Console Instance;

private static readonly Dictionary _commands                = new();
private static readonly Dictionary _cmdHelpDescriptions     = new();
private static          Dictionary _sceneIndex              = new();
private static readonly Dictionary _aliases                 = new();
private static readonly Dictionary _commandToAliasRelations = new();
```

```csharp
// Bad - way messier, takes my brain longer to parse.
const string ToggleAction = "ToggleConsole";
const string SendLineAction = "SendLine";
const string SpectateLeftAction = "SpectateLeft";
const string SpectateRightAction = "SpectateRight";

public const string ConsoleGroup = "gd-console";
public const string SpectateGroup = "CanSpectate";

const string ImaginaryVariable = "1";

private static bool        _isSpectating = false;
private static Array<Node> _spectateList;
private static int         _activeSpectateIdx;

public static Console Instance;

private static readonly Dictionary _commands = new();
private static readonly Dictionary _cmdHelpDescriptions = new();
private static Dictionary _sceneIndex = new();
private static readonly Dictionary _aliases = new();
private static readonly Dictionary _commandToAliasRelations = new();
```

### Commenting
Ideally, the code should be written so that it is self-commenting.

If this is not possible, prefer to append comments directly on the same line as the relevant code

```csharp
int someMysteriousPieceOfCode = 1; // Good
```

```csharp
// Bad
int someMysteriousPieceOfCode = 1;
```

### Formatting standards
todo

### Todo
- Attempt writing an auto-formatter
- Add more examples
- Elaborate stuff
- Provide the most elaborate whys, but hide them away from plain sight to avoid distraction.

