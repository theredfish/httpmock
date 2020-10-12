## Version 0.5.0
- ❌ _**Breaking Change**_: Function `Mock::expect_json_body` was renamed to `expect_json_body_obj`.
- ❌ _**Breaking Change**_: Function `Mock::return_json_body` was renamed to `return_json_body_obj`.
- 🚀 _**Attention**: A new API for mock definition was added. The old API is still available and functional, 
but is deprecated from now on. Please consider switching to the new API._
- 🚀 **Attention**: The following new assertion functions have been added that will provide you smart and helpful 
error output to support debugging:
    - `MockRef::assert`
    - `MockRef::assert_hits`
    - `MockRef::assert_async`
    - `MockRef::assert_hits_async`
- The two methods `MockRef::times_called` and `MockRef::times_called_async` are now deprecated. Consider using
`MockRef::hits` and `MockRef::hits_async`.
- The two methods `Mock::return_body` and `Then::body` now accept binary content.
- The following new methods accept a `serde_json::Value`:
    - `Mock::expect_json_body`
    - `Mock::return_json_body`
    - `When::json_body`
    - `Then::json_body`
- 🔥 Improved documentation (**a lot!**).
- 👏 Debug log output is now pretty printed! 
- 🍪 Cookie matching support.
- Support for convenient temporary and permanent redirect.
- The log level of some log messages was changed from `debug` to `trace` to make debugging easier.

## Version 0.4.5
- Improved documentation.
- Added a new function `base_url` to the `MockServer` structure.