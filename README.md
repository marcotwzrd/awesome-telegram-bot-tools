# Awesome Telegram Bot Tools [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, libraries, and resources for building, debugging, and operating Telegram bots — for developers, channel admins, and OSINT researchers.

This list focuses on **tools you actually use day-to-day** rather than yet-another-tutorial. Everything listed has been verified to work as of 2026.

## Contents

- [Web utilities](#web-utilities)
- [Bot frameworks](#bot-frameworks)
- [Hosting & deployment](#hosting--deployment)
- [Analytics & monitoring](#analytics--monitoring)
- [Channel management](#channel-management)
- [Telegram-native marketplaces](#telegram-native-marketplaces)
- [Official references](#official-references)

## Web utilities

Free in-browser tools you don't need to install. Most run client-side and never see your credentials.

- **[tgkit.io](https://tgkit.io/)** — toolbox covering the whole stack: ID resolver, username checker + history, chat-id guide, bot token tester, inline keyboard builder, MarkdownV2 escaper, error code reference, QR generator, deep link builder, sticker pack downloader, webhook tester, getUpdates viewer, channel post parser, link preview tester, UTM start-param builder, and a live Telegram status page. All free, no signup.
- **[@userinfobot](https://t.me/userinfobot)** — DM it any message, get your numeric user ID back.
- **[@RawDataBot](https://t.me/RawDataBot)** — add to a chat, posts the full chat metadata and message structure.
- **[Telegram Web (k)](https://web.telegram.org/k/)** — the most powerful official web client. Useful for testing bot UIs across viewports.

## Bot frameworks

The libraries we'd actually pick if starting a new bot today.

### Python
- **[python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot)** — the de-facto Python framework. Async-first since v20, well-maintained, exhaustive docs.
- **[aiogram](https://github.com/aiogram/aiogram)** — fully async, Pydantic-validated, FSM built-in. Popular in the bot-trading community.
- **[Telethon](https://github.com/LonamiWebs/Telethon)** — MTProto client (not Bot API). Needed when you must act as a user account: large channel admin operations, account recovery, OSINT.
- **[Pyrogram](https://github.com/pyrogram/pyrogram)** — alternative MTProto client. Mostly community-maintained these days; check recent commits before adopting.

### Node.js / TypeScript
- **[grammY](https://grammy.dev/)** — modern TypeScript-first, plugin ecosystem, great DX. Default pick for new Node bots.
- **[Telegraf](https://telegraf.js.org/)** — older but stable. Massive existing codebase out there.
- **[node-telegram-bot-api](https://github.com/yagop/node-telegram-bot-api)** — minimal, older API.

### Go
- **[go-telegram-bot-api](https://github.com/go-telegram-bot-api/telegram-bot-api)** — standard library-style API, batteries included.
- **[telebot.v3](https://github.com/tucnak/telebot)** — handler-based, route-style.

### Other
- **[teloxide](https://github.com/teloxide/teloxide)** — Rust framework with dialogue management.
- **[Botfather wrappers in PHP / Ruby / .NET / Kotlin]** — most languages have at least one maintained library; check the [official list](https://core.telegram.org/bots/samples).

## Hosting & deployment

Where to actually run your bot in production.

- **Cloudflare Workers** — free tier handles webhook bots up to 100k requests/day. Cold start measured in low ms.
- **Fly.io** — generous free tier, regional control if you need EU/US/APAC presence.
- **Railway / Render** — opinionated PaaS, fastest "git push to live bot" workflow.
- **VPS (Hetzner, OVH, DigitalOcean)** — when you need control over network, file system, or sub-millisecond latency to Telegram DCs.

## Analytics & monitoring

- **[BotFather analytics](https://t.me/BotFather)** — `/mybots → Bot Settings → Bot Statistics` gives free daily message volume and active-user counts.
- **[Combot](https://combot.org/)** — group statistics, member growth, content metrics. Free tier covers most public groups.
- **Custom Prometheus / Grafana** — for high-volume production. Instrument every `sendMessage` for latency + error-code distribution.

## Channel management

- **[OpenSparta](https://opensparta.com/en)** - SaaS workspace for managing connected Telegram accounts and proxies, with relevant conversation discovery.

## Telegram-native marketplaces

Places to find, list, or promote bots and channels.

- **[Fragment](https://fragment.com/)** — official auction for premium usernames, anonymous numbers, and TON-related assets.
- **[Telegram Mini Apps store](https://t.me/tappshub)** — community-curated Mini Apps directory.

## Official references

- **[Bot API documentation](https://core.telegram.org/bots/api)** — the canonical reference. Bookmark the page hash navigation.
- **[MTProto API documentation](https://core.telegram.org/api)** — when the Bot API doesn't expose what you need.
- **[Bot FAQ](https://core.telegram.org/bots/faq)** — the underrated rate-limits + best-practices doc.
- **[Bots: An introduction for developers](https://core.telegram.org/bots)** — concept-level overview.

## Contributing

PRs welcome. Each addition should:

1. Be a tool, library, or resource a Telegram bot developer or channel admin actually uses.
2. Be currently maintained (commit within the last 12 months, or stable enough that nothing needs maintaining).
3. Include a one-line description explaining what makes it worth listing.

No paid promotions accepted. Self-submissions for tools you author are fine — just disclose in the PR.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
