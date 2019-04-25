# server testing

## components of an api

function name(args) => return something;

- routes/endpoints: url(data) => return response;
- business logic (validation/data conversion/operations).
- data access: talk to the persistent data store.

set the test environment to run on 'node' instead of a browser

browser has window => node has global

cross-env = npm package used to abstract away OS differences setting env vars DB_ENV=testing
its dynamically loading a different env file for testing.

when using strings [''] use .toBe in expect and when using objects [api: ''] use .toEqual in expect (this is in (server)spec.js)