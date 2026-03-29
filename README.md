# jasmin-manage-ui

`jasmin-manage-ui` is a React web interface for the JASMIN Projects Portal. It consumes the JASMIN Manage API and provides project, consortium, service, and requirement management views for portal users.

## Scope

The application includes UI flows for:

- browsing project and consortium records
- viewing project detail pages
- creating and joining projects
- reviewing services and requirements
- approving, editing, and deleting requirement items
- handling REST-backed resource forms and instance actions

## Stack

- React 17
- Create React App / `react-scripts`
- React Router
- React Bootstrap
- `fwtheme-react-jasmin`
- Yarn 4
- `http-proxy-middleware` for local API proxying

## Repository structure

```text
src/api/             API wrappers
src/Components/      App pages, detail views, tables, and action components
src/rest-resource/   Shared resource hooks, fetch helpers, and form components
src/css/             Project-specific styling
src/setupProxy.js    Local API proxy configuration
```

## Local development

### Requirements

- Node.js
- Yarn
- A local JASMIN Manage API instance running on `http://localhost:8000`

### Setup

```bash
git clone https://github.com/StTysh/jasmin-manage-ui.git
cd jasmin-manage-ui
yarn install
yarn start
```

The UI starts on `http://localhost:3000`.

## Available scripts

```bash
yarn start   # start development server
yarn build   # create production build
yarn test    # run tests
```

## Notes

- The repository expects the companion JASMIN Manage API to be available locally during development.
- The UI is built around resource-oriented views and actions rather than a standalone backend.
