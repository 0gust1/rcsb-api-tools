# RCSB Saguaro API Changelog

[Semantic Versioning](https://semver.org/)

## [4.0.1] - 2022-04-14
### Bug fixes
- Use `node-fetch` if `window.fetch` is not defined 

## [4.0.0] - 2022-04-13
### Breaking change
- Replaced graphql client `@apollo/client` for `graphql-request`
- `GraphQLRequest` constructor parameters changed
  - `api: "data-api" | "1d-coordinates" | string`
    - `"data-api"` requests to RCSB data-api (https://data.rcsb.org).
    - `"1d-coordinates"` requests to RCSB 1d-coordinate service (https://1d-coordinates.rcsb.org
    - `string` encoding a URL 
  - `config` additional configuration for `GraphQLClient` ('graphql-request' npm package https://www.npmjs.com/package/graphql-request) 
### Improvement
- Library adds caching and data compression at browser side through `localStorage`
  - This feature is not use in the back end

## [3.0.2] - 2022-03-23
### Bug fixes
- JavaScript fetch bug fixed

## [3.0.1] - 2022-03-23
### Dependency update
- Updated several dependencies

## [3.0.0] - 2022-02-14
### Breaking changes
- `GraphQLRequest` exposes `HttpOptions` and `ApolloClientOptions` configurations as optional arguments. 
- Previous ApolloClient config exposed through apollo-boost module is not available anymore

### Dependency update
- Removed apollo-boost v0.4.9
- Update apollo-client v2.6.10 to @apollo/client v3.5.8 

## [2.3.1] - 2022-02-08
### Bug fix
- Fixed server config

## [2.3.0] - 2022-02-08
### RCSB data api schemas
- Added RCSB DW schema interfaces and enumerations

## [2.2.4] - 2022-02-08
### Dependency update
- Updated several dependencies

## [2.2.3] - 2022-02-08
### Bug fixes
- `SearchRequest` initializes `fetch` within the constructor

## [2.2.2] - 2021-12-21
### Configuration improvement
- `GraphQLRequest` exposes ApolloClient configuration as an optional parameter
- `SearchRequest` accepts an external fetch-like request (e.g. node-fetch) as an optional parameter

## [2.2.1] - 2021-10-05
### Build configuration
- Allow JavaScript during TypeScript compile

## [2.2.0] - 2021-10-04
### Chemical Search and bug correction
- Added chemical search metadata schemas
- Added a new regex to include missing enums in search end point

## [2.1.0] - 2021-08-24
### Bug correction
- Yosemite config fixed
- Generation of new types for Yosemite

## [2.0.1] - 2021-07-23
### Bug correction
- Yosemite config fixed

## [2.0.0] - 2021-07-23
### Added search metadata package
- Search data field paths and allowed operations

## [1.1.1] - 2021-07-16
### Dependency Bug
- Fixed production dependencies

## [1.1.0] - 2021-07-16
### Config format
- simplified gql server config

## [1.0.6] - 2021-07-12
### Bug fixes
- yosemite server config fixed

## [1.0.5] - 2021-07-12
### Bug fixes
- apollo-boost dependency added

## [1.0.4] - 2021-07-12
### Bug fixes
- build .json files included

## [1.0.3] - 2021-07-12
### Bug fixes
- graphql dependency added

## [1.0.2] - 2021-07-12
### Bug fixes
- @graphql-codegen/cli dependency added

## [1.0.1] - 2021-07-12
### Bug fixes
- Including js files

## [1.0.0] - 2021-07-12
### General
- Initial release