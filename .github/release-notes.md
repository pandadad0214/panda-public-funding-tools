**Install** from [PyPI](https://pypi.org/project/panda-public-funding-tools/) (needs [uv](https://docs.astral.sh/uv/) and a free [Apify token](https://console.apify.com/settings/integrations)):

```bash
uvx panda-public-funding-tools@{{VERSION}}
```

- **Cursor / Claude / VS Code:** command `uvx`, args `["panda-public-funding-tools"]`, env `APIFY_TOKEN`.
- Official MCP Registry name: `io.github.pandadad0214/panda-public-funding-tools`.

### Added
- `sam_gov_opportunities` and `eu_ted_tenders` (EU tenders moved from leads). This server now has 10 tools.

### Changed
- Syncs with panda-federation-tools 1.8.0 (40 tools across four focused servers). Requires `panda-federation-tools>=1.8.0,<2`.

Full docs: [README](https://github.com/pandadad0214/panda-public-funding-tools#readme).
