# InFlow

InFlow is agentic commerce infrastructure. It gives Agents and Services a common toolchain for
discovery, enrollment, authentication, and payments across MPP and x402.

The InFlow command-line interface gives Agents one entry point for discovering Services, navigating
their Offerings, establishing credentials, and paying protected endpoints. The InFlow software
development kits let applications integrate Buyer and Seller payment workflows directly in
Node.js, Go, Python, and Rust.

## How InFlow works

1. An Agent discovers a relevant Service and the Offerings it exposes.
2. The Agent enrolls when the Service requires identity, claims, or a reusable credential.
3. The Agent invokes a protected Action through MPP or x402.
4. InFlow coordinates authentication, approval, payment, and the resulting receipt.

Services can integrate either payment protocol without replacing their application or catalog.
Agents use a consistent interface while each Service retains control of its access and payment
requirements.

## Open protocol ecosystem

InFlow brings together three complementary layers:

- [Offering Discovery Protocol](https://github.com/offering-protocol) defines how Agents discover
  Services and navigate Collections, Offerings, and Actions.
- [Agent Enrollment Protocol](https://github.com/aep-foundation) defines how Agents establish an
  identity and credential relationship with Services.
- MPP and x402 define how Agents pay protected HTTP endpoints.

Each layer can be adopted independently. Together they support a complete flow from discovery to
enrollment and payment.

## Start here

| Goal                          | Resource                                                               |
| ----------------------------- | ---------------------------------------------------------------------- |
| Learn about InFlow            | [InFlow](https://www.inflowpay.ai/)                                    |
| Install and use the Agent CLI | [InFlow CLI](https://www.inflowcli.ai/)                                |
| Discover Services             | [InFlow Directory](https://directory.inflowpay.ai/)                    |
| Integrate a Service           | [Service integration guide](https://directory.inflowpay.ai/integrate/) |
| Validate a Service            | [Service validator](https://directory.inflowpay.ai/validate/)          |
| Build with an InFlow SDK      | [Software development kits](#software-development-kits)                |

## Software development kits

Choose the language used by your application. Each SDK provides MPP and x402 Buyer
and Seller integrations. Start with its integration guide, then run an example
for the role you need: Buyers pay for resources; Sellers accept payments.

| Language | Integration guide                                                    | Runnable examples                                                                  |
| -------- | -------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Go       | [inflow-go](https://github.com/inflowpayai/inflow-go#readme)         | [Go examples](https://github.com/inflowpayai/inflow-go/tree/main/examples)         |
| Node.js  | [inflow-node](https://github.com/inflowpayai/inflow-node#readme)     | [Node.js examples](https://github.com/inflowpayai/inflow-node#examples)            |
| Python   | [inflow-python](https://github.com/inflowpayai/inflow-python#readme) | [Python examples](https://github.com/inflowpayai/inflow-python/tree/main/examples) |
| Rust     | [inflow-rust](https://github.com/inflowpayai/inflow-rust#readme)     | [Rust examples](https://github.com/inflowpayai/inflow-rust/tree/main/examples)     |

Framework adapters and upstream payment capabilities differ by language. See the
[compatibility and support matrix](https://github.com/inflowpayai/inflow-specs#sdk-compatibility-and-support)
for runtime requirements, dependency declarations, and links to known limitations.
The SDK guides contain installation and account setup instructions. InFlow payment
SDKs do not replace the separate ODP discovery or AEP enrollment SDKs linked above.

## Public repositories

| Repository                                                    | Purpose                                                        |
| ------------------------------------------------------------- | -------------------------------------------------------------- |
| [`inflow-specs`](https://github.com/inflowpayai/inflow-specs) | Public SDK contracts, conformance artifacts, and compatibility |
| [`inflow-cli`](https://github.com/inflowpayai/inflow-cli)     | Agent CLI, Model Context Protocol server, and agent skills     |
| [`homebrew-tap`](https://github.com/inflowpayai/homebrew-tap) | Homebrew distribution for the InFlow command-line interface    |

Implementation bugs and language-specific integration questions belong in the corresponding
software development kit repository. Command behavior, agent skills, and terminal integration
questions belong in `inflow-cli`.
