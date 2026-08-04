# Bytestrone MVC to Web API

## Overview
This codemod automates the architectural transition of legacy ASP.NET MVC Controllers (which return HTML Views) into stateless RESTful **Web API** Controllers (which return JSON).

## How It Works
It performs AST-based replacements to decouple the backend logic from the frontend presentation layer:
* **Controller Refactoring:** Changes base classes from `Controller` to `ControllerBase` (or `ApiController`).
* **Return Type Transformation:** Replaces legacy `return View(model)` syntax with `return Ok(model)` or equivalent JSON response wrappers.
* **Namespace Modernization:** Cleans up obsolete `System.Web.Mvc` references in favor of HTTP API routing namespaces.

## Usage
```bash
npx codemod run bytestrone-mvc-to-web-api
```
