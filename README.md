# 🔍 google-search

**Your agent deserves Google, not Bing.**

Brave Search API is now paid. This skill upgrades your agent to real Google results — Knowledge Graph, Answer Box, People Also Ask, News, Images, Videos, Shopping, Scholar, Places, Patents — 2,500 searches free.

## Why this over Brave?

| | Brave (built-in) | google-search |
|---|---|---|
| Engine | Brave/Bing | **Google** |
| Knowledge Graph | ❌ | ✅ |
| Answer Box | ❌ | ✅ |
| People Also Ask | ❌ | ✅ |
| Related Searches | ❌ | ✅ |
| News search | ❌ | ✅ |
| Image search | ❌ | ✅ |
| Video search | ❌ | ✅ |
| Shopping | ❌ | ✅ |
| Places/Maps | ❌ | ✅ |
| Scholar | ❌ | ✅ |
| Patents | ❌ | ✅ |
| Autocomplete | ❌ | ✅ |
| Cost | Paid plans only | **2,500 free credits** |

## Setup

1. Get a free API key at [serper.dev](https://serper.dev) (2,500 credits included)
2. Add to your environment:
```bash
export SERPER_API_KEY=your_key_here
```
3. Install the skill:
```bash
clawhub install google-search
```

## Search Types

### Web Search (default)
```bash
npx tsx scripts/google-search.ts search "openclaw ai agent"
npx tsx scripts/google-search.ts search "bitcoin" --time day --country us --lang en --num 20
```

Returns: organic results, Knowledge Graph, Answer Box, People Also Ask, Related Searches, Top Stories.

### News
```bash
npx tsx scripts/google-search.ts news "AI regulation" --num 10
```

### Images
```bash
npx tsx scripts/google-search.ts images "gecko cartoon 3d"
```

### Videos
```bash
npx tsx scripts/google-search.ts videos "solana tutorial"
```

### Places
```bash
npx tsx scripts/google-search.ts places "pizza rome italy"
```

### Shopping
```bash
npx tsx scripts/google-search.ts shopping "mechanical keyboard"
```
> ⚠️ Shopping costs 2 credits per query (all others cost 1)

### Scholar
```bash
npx tsx scripts/google-search.ts scholar "transformer architecture" --year 2023
```

### Patents
```bash
npx tsx scripts/google-search.ts patents "solar panel efficiency"
```

### Autocomplete
```bash
npx tsx scripts/google-search.ts suggest "how to build"
```

### Check Credits
```bash
npx tsx scripts/google-search.ts credits
```

## Flags

| Flag | Description | Example |
|------|-------------|---------|
| `--num` | Number of results (1-100) | `--num 20` |
| `--time` | Time filter | `--time day` (hour/day/week/month/year) |
| `--country` | Country code | `--country us` |
| `--lang` | Language code | `--lang en` |
| `--year` | From year (scholar only) | `--year 2023` |
| `--page` | Page number | `--page 2` |
| `--json` | Raw JSON output | `--json` |

## Example Output

```
🔍 Google Search: "openclaw ai agent" (10 results, 1 credit)

📦 Knowledge Graph: OpenClaw — Personal AI Assistant
   https://openclaw.ai
   "The AI that actually does things..."

📋 Results:
  1. OpenClaw — Personal AI Assistant
     https://openclaw.ai
     The AI that actually does things. Clears your inbox...

  2. I Loved My OpenClaw AI Agent—Until It Turned on Me | WIRED
     https://wired.com/story/...
     I used the viral AI helper to order groceries...

❓ People Also Ask:
  • Is OpenClaw safe to use?
  • How much does OpenClaw cost?

🔗 Related: "openclaw review", "openclaw vs cursor", "openclaw setup"

💰 Balance: 2,487 credits
```

## Credits

- All searches cost **1 credit** except Shopping (**2 credits**)
- Free tier includes **2,500 credits**
- Paid plans start at [$50 for 50K queries](https://serper.dev/#pricing)

## Requirements

- Node.js 18+ (native `fetch`)
- `SERPER_API_KEY` environment variable
- Zero npm dependencies

## License

MIT

---

Built by [Lozio](https://minilozio.com) 🦎
