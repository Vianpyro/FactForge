# FactForge

**FactForge** is a self-hostable, open-source Rust app delivering TikTok/Instagram-style infinite scrolls of politically neutral, fact-checked knowledge. Tired of biased news and unverified social media? Forge your own feed of verifiable facts from trusted sources like AP, Reuters, Britannica, and Our World in Data—perfect for you, your family, friends, and the world.

## ✨ Why FactForge?

Escape algorithmic echo chambers with a battle-tested foundation for intellectual social media. Built in Rust for performance and safety, FactForge pulls fresh, neutral content via free APIs/RSS, supports offline networks of self-hosted instances, and invites global contributions to truth.

### 🎯 Key Features

1. **🤖 Neutral Fact Feeds**
   - Hourly cron pulls from AP, Reuters, Britannica, Wikidata, Our World in Data
   - Image proxying (no hotlinking); short-form cards for easy scrolling
   - Cross-verified claims via Google Fact Check Tools API

2. **🔗 Self-Hostable & Resilient**
   - Dockerized Rust backend; dev container ready
   - P2P-ready for fact networks (future: offline sync)
   - Single-server start, scales to federated instances

3. **🛠️ Open-Source Collaboration**
   - Rust + modern web stack; contribution-friendly
   - Automated linting (clippy, rustfmt), CI/CD via GitHub Actions
   - Branch validation, PR templates, rich labels

4. **📱 Simple Intellectual UX**
   - Infinite scroll of facts (science, history, stats, news)
   - No ads, no bias—community-flagged via future notes
   - Mobile-first like Instagram/TikTok

## 🚀 Getting Started

### Using This Template

1. **Clone & setup:**
   ```bash
   git clone https://github.com/YOUR-USERNAME/factforge.git
   cd factforge
   ```

3. **Run locally:**
   ```bash
   docker compose up  # Dev environment
   # Visit localhost:8283 for your fact feed
   ```

### Quick Self-Host

```bash
# Production
make build
docker run -p 8283:8283 yourusername/factforge:latest
```

## 📁 What's Included

- **Rust Workspace**: `src/` bin + lib; Cargo.toml with axum/tokio/serde
- **`.devcontainer/`**: Full-stack dev (Rust, Node for frontend if needed)
- **`.github/workflows/`**: Linting, tests, Docker builds, releases
- **Templates**: Issues/PRs with checklists for fact-source PRs

## 🔧 Customization

- **Add Sources**: Edit `sources.toml` → AP RSS, Wikidata SPARQL
- **Rust Tweaks**: `Cargo.toml` for crates; clippy enforces safety
- **Deploy**: Railway/Fly.io/Hetzner; scale to P2P later

**Branch Convention**: `feature/fact-source-ap` | `fix/bias-check` | `chore/dockerfile`

## 🤝 Contributing

1. Fork → `feature/your-idea`
2. Add neutral sources with verification
3. PR with fact samples + bias rating (AllSides/Ad Fontes)
4. Follow Rust style; tests required

**Guidelines**: Only verifiable, neutral content. No opinions. MIT License.

## 📝 License

MIT – Permissive for self-hosting/networks. See [LICENSE](LICENSE).

## 🐛 Troubleshooting

- **Cron fails**: Check API quotas (NewsAPI free tier)
- **Rust errors**: `cargo clippy --fix`
- **Bias flags**: Cross-check AllSides; PR fixes

**Forge facts, not fights. Join the neutral network!** 🚀
