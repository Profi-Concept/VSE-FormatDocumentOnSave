VSE-FormatDocumentOnSave
========================
Enables auto formatting of the code when you save a file. Visual Studio supports auto formatting of the code with the CTRL+E,D or CTRL+E,F key shortcuts but with this extension the command `Edit.FormatDocument` is executed on Save.

# Download
https://marketplace.visualstudio.com/items?itemName=mynkow.FormatdocumentonSave

# Configuration
There are 3 settings which you could configure:
* Command
* Allowed extensions
* Denied Extensions

### Command
This is the Visual Studio command which will be invoked when a document is saved.
##### Default
`Edit.FormatDocument`

### Allowed extensions
Specifies all file extensions where the `command` is allowed to be executed. For multiple values you could use `space` separated list.
##### Default
`allowed_extensions = .*`

### Denied extensions
Specifies all file extensions where the `command` is NOT allowed to be executed. For multiple values you could use `space` separated list.
##### Default
`denied_extensions = `

# Examples
## Scenario 1
- `allowed_extensions = .*`
- `denied_extensions = .cs` 

**Result:** All documents will be formatted because we explicitly specified that all extensions will be formatted using `allowed_extensions = .*`.

## Scenario 2
- `allowed_extensions = `
- `denied_extensions = .js` 

**Result:** All documents will be formatted except those with `.js` extension

## Scenario 3
- `allowed_extensions = `
- `denied_extensions = .*` 

**Result:** No documents will be formatted

## Scenario 4
- `allowed_extensions = .cs`
- `denied_extensions = ` 

**Result:** Only documents with `.cs` extension will be formatted

# Visual Studio
You can configure these settings from the Visual Studio Options menu

# Format Config

`.formatconfig`
```
root = true

[*.*]
command = Edit.FormatDocument
allowed_extensions = .*
denied_extensions = .js .html
```
