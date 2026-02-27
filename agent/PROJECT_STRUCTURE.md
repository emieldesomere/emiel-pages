# Project Structure Rules

## Root

- `/index.html`
  Displays a list of available applications.
  Links to each application.

- `/apps.json`
  Contains metadata for all applications.
  Used by index.html to render the app list.

- `/apps/`
  Contains one subfolder per application.

## Application Folder

Each application must be in:

/apps/<application-name>/

Each app should contain at minimum:
- index.html
- optional JS files
- optional CSS files
- optional assets folder

The application must:
- Run standalone
- Not depend on external servers
- Contain an obvious "Exit" button
- Exit button returns to `/index.html`

## Deleting Applications

Applications must NEVER be physically deleted.

To hide an application:
- Set `"visible": false` in apps.json

index.html must only render apps where:
"visible": true
