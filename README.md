# VM0 Content Farm Agent

An AI-powered blog content generation agent that automatically creates high-quality, SEO-optimized articles in Japanese from trending news sources.

## Features

- Fetches news from multiple RSS sources (Hacker News, TechCrunch, Wired, etc.)
- Generates SEO-optimized titles and outlines in Japanese
- Writes 1000-1500 word articles in Japanese with proper citations
- Creates featured images using AI
- Publishes directly to Qiita

## Usage

Run the agent with a topic:

```bash
vm0 run content-farm --artifact-name my-blog "Write an article about the latest AI developments"
```

## Required Secrets

Configure these secrets in your VM0 account:

| Secret | Description |
|--------|-------------|
| `CLAUDE_CODE_OAUTH_TOKEN` | Claude Code OAuth token |
| `FAL_KEY` | fal.ai API key for image generation |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary cloud name |
| `CLOUDINARY_API_KEY` | Cloudinary API key |
| `CLOUDINARY_API_SECRET` | Cloudinary API secret |
| `QIITA_ACCESS_TOKEN` | Qiita personal access token for publishing |

## Workflow

The agent follows an 8-phase workflow:

1. **Gather News** - Fetch articles from RSS feeds
2. **Filter and Select** - Pick relevant articles for the topic
3. **Create SEO Title** - Generate optimized title candidates in Japanese
4. **Build Outline** - Structure the article
5. **Write Article** - Create the full content in Japanese
6. **Generate Image** - Create a featured image
7. **Prepare Output** - Save all artifacts
8. **Publish** - Post to Qiita

## Auto-Publishing

This repository uses [vm0-ai/compose-action](https://github.com/vm0-ai/compose-action) to automatically publish the agent configuration on every push to main.

## License

MIT
