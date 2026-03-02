# AI Ecosystem Power Map — Top 100

An interactive force-directed graph mapping the 100 most important companies, people, and power flows in the AI industry (2025).

## Live Demo

Open index.html in your browser, or deploy to GitHub Pages (see below).

## Features

- Market-cap sized nodes — Apple ($3.5T) is massive, startups are small
- Click any node for a detail panel with photos, bios, key contributions, and connections
- Color-coded edges — Blue (funding), Green (compute/chips), Red dashed (talent moves), Purple (partnerships)
- Search by name, company, or tag (try "safety", "GPU", "transformer")
- Filter by tier — S-Tier only, A-Tier, or show all
- Drag nodes to rearrange, scroll to zoom, toggle labels/edges
- Hover to highlight all connections

## What's Mapped

- 12 S-Tier Companies: NVIDIA, Microsoft, Apple, Google, OpenAI, Anthropic, Meta, Amazon, TSMC, AMD, xAI, DeepMind
- 7 Other Majors: Tesla, Palantir, Broadcom, IBM, Bytedance, DeepL
- 25 Hot Startups: Cursor, Mistral, Perplexity, ElevenLabs, Midjourney, Databricks, HuggingFace, and more
- 30+ Key People: Sam Altman, Jensen Huang, Demis Hassabis, Yann LeCun, and more
- 15 Influencers: Andrew Ng, Lex Fridman, Andrej Karpathy, Ethan Mollick, and more
- 60+ Connections: Funding, Compute, Talent Moves, Partnerships, Products

## Deploy to GitHub Pages

1. Create a new repo on GitHub (e.g. ai-power-map)
2. Upload index.html (the interactive map file) and this README
3. Go to Settings > Pages
4. Under Source, select Deploy from a branch
5. Choose main branch, / (root) folder
6. Click Save
7. Your map will be live at https://YOUR-USERNAME.github.io/REPO-NAME/

No build step needed — it's a single HTML file. D3.js loads from CDN.

## Contributing

PRs welcome! Here's what would make this better:

- More connections — there are always more edges to add
- Updated valuations — market caps change daily
- New companies/people — the ecosystem evolves fast
- Better photos — use Wikimedia Commons URLs
- Chinese AI ecosystem — Baidu, Alibaba, DeepSeek, Zhipu AI
- European AI — Aleph Alpha, Mistral ecosystem, EU policy makers
- Timeline view — show how the ecosystem evolved over time
- Mobile optimization — touch gestures for phone/tablet

### How to add a node

In the nodes array in index.html, add:

{
  id: "UniqueID",
  label: "Display Name",
  type: "startup",          // s-company | startup | other-company | s-person | a-person | bc-person
  group: "Startup",
  tier: "A",                // S | A | B | C
  mcap: 10,                 // Market cap/valuation in billions (0 for people)
  img: "https://...",       // Optional photo URL
  role: "Short description",
  why: "Why they matter paragraph",
  facts: "HTML formatted key facts",
  tags: ["Tag1", "Tag2"]
}

### How to add a connection

In the links array, add:

{
  source: "NodeID1",
  target: "NodeID2",
  type: "partnership",      // leads | funding | compute | talent | partnership | product
  label: "Short description"
}

## Data Sources

Market caps and valuations are approximate (early 2025). Startup valuations based on last known funding rounds. All information from public sources.

## License

MIT — use it however you want.
