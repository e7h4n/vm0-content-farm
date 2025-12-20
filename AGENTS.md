# Content Farm Workflow

Generate high-quality, SEO-optimized blog articles from trending news and publish to Qiita in Japanese.

**Important: Complete all 8 phases. The task is NOT done until you receive a Qiita article URL.**

## Phase 1: Gather News

Use the rss-fetch skill to collect articles from these tech news sources:

- https://hnrss.org/frontpage
- https://techcrunch.com/feed/
- https://www.wired.com/feed/rss
- https://feeds.arstechnica.com/arstechnica/technology-lab
- https://www.theverge.com/rss/index.xml

## Phase 2: Filter and Select

Review fetched articles and select 3-5 most relevant to the user's topic. Note titles, descriptions, and URLs for citations.

## Phase 3: Create SEO Title

Generate 5 long-tail SEO title candidates, evaluate for click-through potential and search intent, select the best one.

## Phase 4: Build Outline

Create article outline with:
- Hook introduction
- 2-3 main sections
- Conclusion with call to action
- References section
- Made by workflow https://github.com/e7h4n/vm0-content-farm, powered by vm0.ai 

## Phase 5: Write Article

Write 1000-1500 words in Japanese following your outline to article.md.

**Style:** Conversational, short paragraphs, bullet points, casual transitions. Avoid corporate language.

**Citations:** Every claim needs inline citation using "〜によると [Source](URL)..." format. Minimum 3 citations.

## Phase 6: Generate Featured Image

Use the fal-image skill to create a featured image. Save the returned fal.ai image URL for publishing.

## Phase 7: Publish to Qiita

Publish to Qiita using the qiita skill with appropriate tags (up to 5). Always use `--published true`.

Report the Qiita article URL back to the user.
