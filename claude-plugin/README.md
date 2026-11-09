# SOS Flights plugin for Claude

Get to your destination when your flight breaks. This plugin bundles the hosted SOS Flights MCP server with a skill that tells Claude how to help a traveller whose flight is cancelled, delayed, overbooked or who missed a connection.

## What it does

- Checks passenger rights under EU261, UK261 and US DOT rules: refund or re-routing, the care the airline owes (meals, hotel) and the compensation range with its conditions. Advice only, not legal advice.
- Writes 1–3 short sentences to say at the airline desk, in the traveller's language.
- Lists hotel, lounge and transfer links for about 100 airports and nearby alternative airports.
- Searches live alternative flights, including airports within 300 km and rail links for shorter trips. Nothing is booked.
- When the airline won't help, prepares a case for the SOS Flights expert team. A case is opened only after the traveller confirms it, and is a paid one-time service unless a travel-agency access code covers it.

## What it connects to

One remote MCP server, `https://www.sosflights.help/mcp` (Streamable HTTP, no sign-in), operated by pelicantravel.com s.r.o. The plugin runs no local code, hooks or scripts. Tool calls send the flight details you give Claude to that server; preparing and opening a case also sends the email, phone and situation summary the traveller provides.

## Privacy Policy

https://www.sosflights.help/en/privacy

## Support

info@sosflights.help · https://www.sosflights.help/en/connect

## License

MIT
