# Security Policy

This policy applies to every repository in the Labelixa organization
unless a repository ships its own SECURITY.md.

## Reporting a vulnerability

Please report suspected security issues privately by email to
**support@labelixa.com**. Do not open a public GitHub issue for a
vulnerability.

Machine-readable contact: <https://labelixa.com/.well-known/security.txt>.
Full policy: <https://labelixa.com/security>.

When you report, please include: the affected surface (URL, endpoint,
package, or repository), a description of the issue, and steps or a proof
of concept that let us reproduce it. Please do not run denial-of-service
tests, access other users' data, or modify production data.

## Scope

- The Labelixa web application and API (`labelixa.com`, `api.labelixa.com`)
- The MCP server (`api.labelixa.com/mcp`) and the `labelixa-mcp` bridge
- Published packages: npm `labelixa`, `labelixa-mcp`; PyPI `labelixa`;
  the VS Code extension; the printer agent binaries
- All public repositories of the Labelixa organization, including the
  GitHub Action, the assistant rule files and the installer repositories
  (Homebrew tap, Scoop bucket, Chocolatey packages)

## Response

We aim to acknowledge reports within a few business days and to keep you
updated while we investigate and remediate. We appreciate coordinated
disclosure and will credit reporters who wish to be named.
