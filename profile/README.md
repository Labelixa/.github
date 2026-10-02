Labelixa
Labelixa is a thermal label rendering and validation service: render, validate, debug and convert ZPL, EPL, TSPL and CPCL label code in the browser, through a REST API or from AI assistants over MCP, and generate barcodes — no printer required.

labelixa.com · Documentation · API reference · Status

What we build
ZPL preview and validation — render ZPL at 6, 8, 12 or 24 dpmm; structured diagnostics with stable rule IDs, line positions and severity.
Conversion — ZPL to PNG/PDF, between printer resolutions (203 ↔ 300 ↔ 600 dpi), image to ZPL, TrueType font to ~DU.
Barcodes — standalone barcode images, plus verification of a printed label from a photo.
Other printer languages — EPL, TSPL and CPCL viewers and linters, and printer-language detection.
DirectPrint — a small agent you run on your own network collects print jobs from the Labelixa API and passes them to network printers or to printers on the operating system's print queue (for example USB). It opens no inbound port. Download
Reference material — a ZPL command reference and a printer database where every compatibility claim carries the evidence tier it rests on.
Everything is server-rendered and no printer is needed for preview, validation or conversion. The render is a server-side interpretation of the ZPL command reference — not a guarantee of a specific printer's physical output.

For AI assistants (MCP)
Labelixa runs a remote Model Context Protocol server at https://api.labelixa.com/mcp (streamable HTTP, stateless). Anonymous use is free and rate-limited; an API key uses the account's own quota.

LLMs can write ZPL but cannot see the result. The MCP server closes the write → preview → fix loop inside the conversation.

There is also a local stdio package on npm for clients that prefer one. The remote endpoint and the npm package are two separate products with different tool sets — check the one you are connecting to.

Packages
where	package
npm	labelixa (JS SDK) · labelixa-mcp (local MCP server)
PyPI	labelixa (Python SDK)
VS Code	Labelixa ZPL
MCP directories	Glama · Smithery · MCPBeat
Open repositories here
zpl-examples — working, tested Zebra ZPL label examples (shipping labels, barcodes, QR) with curl / Python / Node / C# integration snippets.
thermal-printer-examples — working TSPL, EPL and CPCL label examples, linted and rendered against a live engine in CI.
thermal-printer-cheatsheets — ZPL, TSPL, EPL and CPCL command cheatsheets, generated from a tested implementation, with honest per-command render coverage.
awesome-thermal-printing — a curated list of tools, references and specifications for thermal label printing.
labelixa-agent-releases — Labelixa DirectPrint agent: released binaries with checksums. Source code is private.
labelixa-mcp — source of the labelixa-mcp npm package: a local stdio MCP server that calls the Labelixa API. MIT.
The application itself is not open source.

How we talk about evidence
Compatibility claims in the printer database are labelled with where they come from: the vendor's manual, our own rendering, or a label actually printed on real hardware and read back. Physical verification exists for a small number of devices and is scoped to the exact model and firmware it was measured on — it is never generalised to a printer family.

If a page does not know something, it says so rather than guessing.

Contact
support@labelixa.com · Part of Newempo LLC
