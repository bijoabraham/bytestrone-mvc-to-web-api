# bytestrone-mvc-to-web-api

This is a native Codemod bundle that leverages the `ast-grep` engine to automate the syntax transformation of ASP.NET MVC controllers into ASP.NET Core Web API controllers.

## Included Rules
1. `scaffold-api.yml`: Converts classes inheriting from `Controller` to `ControllerBase` and injects API attributes.
2. `swap-verb.yml`: Injects HTTP verb attributes (like `[HttpGet]`) based on action names.
3. `action-result.yml`: Standardizes return types to `IActionResult`.
4. `view-returns.yml`: Converts legacy `return View();` to `return Ok();`.
