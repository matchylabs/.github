<h3 align="center">Threat Intelligence, Everywhere You Work</h3>

<p align="center">
  Open source tools to integrate threat intelligence into your existing security workflows, log pipelines, and analysis tools.
</p>

<p align="center">
  <a href="https://matchylabs.com">Website</a> &bull;
  <a href="https://matchylabs.com/matchy/">Documentation</a> &bull;
  <a href="mailto:hello@matchylabs.com">Contact</a>
</p>

---

## What We Build

Most organizations have access to threat intelligence feeds but struggle to use them effectively. The data sits unused while security teams manually hunt through logs.

We build tools that change that. Our software plugs into the data pipelines you already run, automatically matching indicators of compromise against your logs, network traffic, and security data.

## Matchy

Our flagship project. A fast IoC matching engine that builds memory-mapped databases from threat intel feeds.

- **Sub-millisecond lookups** on 100K+ indicators
- **Unified database** for IPs, CIDRs, domains, hashes, and glob patterns
- **CLI, Rust library, and C API** for integration anywhere
- **MaxMind MMDB compatible** - works with existing tooling

```bash
# Build a threat database
matchy build threats.csv -o threats.mxy

# Scan logs for matches
matchy match threats.mxy access.log

# Query individual indicators
matchy query threats.mxy 1.2.3.4
```

<p>
  <a href="https://github.com/matchylabs/matchy"><img src="https://img.shields.io/github/stars/matchylabs/matchy?style=social" alt="GitHub Stars"></a>
  &nbsp;
  <a href="https://crates.io/crates/matchy"><img src="https://img.shields.io/crates/v/matchy.svg" alt="Crates.io"></a>
</p>

**[Get Started with Matchy →](https://github.com/matchylabs/matchy)**

## Pipeline Integrations

Drop threat intelligence matching into your data pipelines:

| Integration | Description |
|-------------|-------------|
| [**elasticsearch-matchy-ingest-plugin**](https://github.com/matchylabs/elasticsearch-matchy-ingest-plugin) | Elasticsearch ingest processor |
| [**fluent-bit-matchy**](https://github.com/matchylabs/fluent-bit-matchy) | Fluent Bit WASM filter plugin |
| [**zeek-matchy-plugin**](https://github.com/matchylabs/zeek-matchy-plugin) | High-performance Zeek plugin (7M+ queries/sec) |
| [**matchy-java**](https://github.com/matchylabs/matchy-java) | Java wrapper for JVM integration |

## Analysis Tools

| Tool | Description |
|------|-------------|
| [**matchy-wireshark-plugin**](https://github.com/matchylabs/matchy-wireshark-plugin) | Real-time threat matching in Wireshark |

## Get Involved

<a href="https://github.com/matchylabs/matchy"><img src="https://img.shields.io/badge/Star_Matchy-181717?logo=github&logoColor=white" alt="Star on GitHub" height="28"></a>
&nbsp;&nbsp;
<a href="https://matchylabs.com"><img src="https://img.shields.io/badge/Join_Mailing_List-4285F4?logo=mail.ru&logoColor=white" alt="Join Mailing List" height="28"></a>

We're open to contributions. Check out [CONTRIBUTING.md](https://github.com/matchylabs/matchy/blob/main/CONTRIBUTING.md) in any repo to get started.
