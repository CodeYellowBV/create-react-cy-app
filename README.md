# Create React CY App [![Build Status](https://travis-ci.org/CodeYellowBV/create-react-cy-app.svg?branch=master)](https://travis-ci.org/facebookincubator/create-react-app)

Create React apps with no build configuration.

* [Getting Started](#getting-started) – How to create a new app.
* [User Guide](https://github.com/CodeYellowBV/create-react-cy-app/blob/master/packages/react-cy-scripts/template/README.md) – How to develop apps bootstrapped with Create React App.

- - -

**This is a fork of [Create React App](https://github.com/facebookincubator/create-react-app), intended for use at our company Code Yellow B.V.**

The main differences with Create React App are;

Changes with create-react-app
- No CSS Autoprefixer, we only support modern browsers
- Uses cache-loader to cache Babel output
- Doesn't use source maps by default
- Support for `PUBLIC_URL` env variable in dev
- Allows module resolving from src/ (e.g. `import 'components/foo'` works everywhere)
- Uses [Babel Minify](https://github.com/webpack-contrib/babel-minify-webpack-plugin) instead of UglifyJs for minifying
- Basic Electron compatibility via env variable
- Allows custom dotenv file location (in our build system `.env` cannot live in the repository root)
- Includes env variables in frontend build with prefix `CY_FRONTEND_*` instead of `REACT_APP_*`
- Babel preset:
  - Less transpiling (we don't have to support many browsers), but still possible to enable a little bit more transpiling via an env variable
  - Uses styled-components babel plugin
  - Uses decorator babel plugin

