# SOS Flights — directory submission kit

Shared texts (English, same everywhere):

- **Name:** SOS Flights
- **Tagline / one-liner:** Get to your destination when your flight breaks
- **Short description:** SOS Flights helps travellers with a cancelled, delayed, overbooked or missed-connection flight find the fastest realistic way to their destination, and puts a human expert team on the case when the airline won't help.
- **MCP description (≤100 chars):** Live reroutes, desk scripts, airport help and EU261/UK261/US DOT rights for disrupted flights.
- **MCP server:** https://www.sosflights.help/mcp (Streamable HTTP, no auth)
- **Website:** https://www.sosflights.help/ · **Connect guide:** https://www.sosflights.help/en/connect · **Docs:** https://www.sosflights.help/mcp.md
- **Privacy:** https://www.sosflights.help/en/privacy · **Terms:** https://www.sosflights.help/terms · **Support:** info@sosflights.help
- **Category:** Travel (else Productivity) · **Publisher:** pelicantravel.com s.r.o.
- **Icon/logo:** chatgpt-plugin/assets/logo.png (512×512), icon.png (192×192)

## Status

| Directory | Status | Who submits | What's needed |
|---|---|---|---|
| Official MCP Registry | ✅ live: `io.github.codeblockssk/sosflights` 0.1.0 | CI (GitHub OIDC) | bump `version` in server.json on every change |
| Claude Connectors Directory | ready to submit | paid Claude account, claude.ai/directory/manage | paste texts below; no test account (no auth) |
| Claude plugin directory | package in `claude-plugin/` (`claude plugin validate` passes) | paid Claude account, same portal → Plugin bundle → repo `codeblockssk/sosflights`, path `claude-plugin` | GitHub connected in the portal |
| ChatGPT apps/plugins directory | package in `chatgpt-plugin/` (zip it) | OpenAI org owner, verified business (platform.openai.com) | domain-verification token on www.sosflights.help, demo video URL |
| Meta Muse connector platform | texts below | Meta developer account | check current form fields |
| Grok Bot Marketplace | waiting for the SOS Grok bot template | — | build the template first |

## Claude Connectors Directory (remote MCP)

Portal: https://claude.ai/directory/manage → Submit → Remote MCP server.

- Server URL: `https://www.sosflights.help/mcp`
- Name (≤100): SOS Flights
- One-liner (≤200): Passenger rights, airline-desk scripts, airport help and live reroutes when your flight is cancelled, delayed or overbooked — plus an expert team when the airline won't help.
- Description (≤2000): use the ChatGPT longDescription from chatgpt-plugin/plugin.json plus: "No sign-in. Advice only, not legal advice. Cases are prepared first and opened only after the traveller confirms; a case is a paid one-time service or covered by a travel-agency access code."
- Categories: Travel
- Authentication: not required
- Tool annotations: all 9 tools have `title`, `readOnlyHint`, `destructiveHint` (checked live). Write tools: `sos_open_case`, `sos_send_message`; both require a `confirmation_token` from the matching prepare tool.
- Test & launch: no test account needed (no auth). Reviewer steps: add the server as a custom connector, ask "My Ryanair BTS–STN flight is cancelled, what are my rights?", "What do I say at the desk?", "Where can I sleep at VIE tonight?", "Find another way VIE to LHR tomorrow". For `sos_prepare_case` use test@example.com; do NOT confirm `sos_open_case` unless the SOS team is told (it creates a real case and payment link).
- Compliance: financial transactions acknowledgment applies (paid case via external payment page).

## ChatGPT

1. platform.openai.com → organization settings → verify business (pelicantravel.com s.r.o.).
2. Zip `chatgpt-plugin/` and upload it in the plugin submission portal; the manifest pre-fills listing, test cases and countries.
3. Domain verification: the portal shows a token; it must be served as plain text at the URL shown on www.sosflights.help (add it to `public/` in the GitLab repo and deploy).
4. Record a short demo video of the 5 positive test cases and add its URL.

## Meta Muse

Muse users can already add SOS as a Custom Connector with the URL above (no review). For the directory listing, submit through Meta's connector platform with the shared texts; Meta tests end to end.
