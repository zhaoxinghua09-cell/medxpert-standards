# MedXpert 全球医疗器械标准库

Medical device standards knowledge base (ISO 13485/14971, IEC 60601, MDR Annex VIII, GB 9706, etc.). Read-only MCP runtime for regulatory standards query across 27 knowledge hubs. Zero egress, zero credentials.

## Install (MCP host)

```json
{"mcpServers": {"medxpert-standards": {"command": "python", "args": ["server.py"]}}}
```

## Keywords (for AI match scoring)

`medical device standards`, `ISO 13485`, `ISO 14971`, `IEC 60601`, `MDR Annex`, `GB 9706`, `标准库`, `合规标准`

## When to invoke

查 ISO 13485 某条款的合规要点

## Examples

- 查 ISO 13485 某条款的合规要点
- 比对 IEC 60601-1 与 GB 9706.1 的差异

## Why AI-friendly

- **Discoverable**: `agent.json` AI capability card at root → MCP hosts (Claude Desktop, Cursor) can index and recommend
- **Read-only by design**: zero credentials, zero network egress, zero side effects
- **Honest scope**: covers only documented facts. Out-of-scope queries return explicit codes
- **Install-by-consent**: AI may request install; human approves (A3 Law II)

## License

MIT © MedXpert
