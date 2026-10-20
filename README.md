# SOS Flights MCP server

**Get to your destination when your flight breaks.**

SOS Flights helps travellers with a cancelled, delayed, overbooked or missed-connection flight find the fastest realistic way to their destination, and puts a human expert team on the case when the airline won't help.

This repository describes the public, hosted SOS Flights MCP server. It contains no server source code — the server runs at:

```
https://www.sosflights.help/mcp
```

- Transport: Streamable HTTP
- Authentication: none (no sign-in, no API key)
- Website: https://www.sosflights.help/
- Connection guide: https://www.sosflights.help/en/connect
- MCP docs: https://www.sosflights.help/mcp.md

## Tools

| Tool | What it does |
|------|--------------|
| `sos_check_rights` | Checks a cancelled, delayed, overbooked or missed-connection flight against EU261, UK261 and US DOT rules. |
| `sos_desk_script` | Writes 1–3 short, polite sentences to say to the airline agent (re-routing, care or refund). |
| `sos_airport_help` | Hotel, lounge and transfer links for an airport, nearby alternative airports, and who pays for a hotel. |
| `sos_find_alternatives` | Searches live one-way flights from the traveller's airport and airports within 300 km to the destination. |
| `sos_prepare_case` | Checks the details for a case handled by the SOS Flights expert team and returns what will be submitted. |
| `sos_open_case` | Opens the prepared case after the traveller confirms it; returns the case code. |
| `sos_get_case` | Returns the status of a case by its case code. |
| `sos_prepare_message` | Prepares a message from the traveller to the SOS Flights team on an active case. |
| `sos_send_message` | Sends the prepared message after the traveller confirms it. |

Rights, desk scripts, airport help and alternative flights are free. A case handled by the SOS Flights team is a paid service; it is opened only after the traveller confirms and pays.

## Connect

See [CONNECT.md](CONNECT.md) for Claude, ChatGPT, Cursor, VS Code and other MCP clients.

## License

The contents of this repository (documentation and metadata) are MIT licensed. The SOS Flights service itself is operated by pelicantravel.com s.r.o.
