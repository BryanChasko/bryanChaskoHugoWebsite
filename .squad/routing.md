# Routing Table — bryanchasko.com

## Pattern → Agent

| Pattern | Route To | Notes |
| ------- | -------- | ----- |
| Hugo config, front matter, content structure | Stratia | Architecture decisions |
| `layouts/` template changes | Stratia + @copilot | Stratia reviews, @copilot implements |
| `assets/css/` changes | @copilot | Use existing CSS variables only |
| WebGL / shader changes | Stratia | Requires careful review for 3D scenes |
| S3 bucket policy, CORS | Myrren | Security-sensitive |
| CloudFront config, cache behaviors | Myrren | JSON in `infrastructure/` |
| DNS / Route 53 | Myrren | Validate before applying |
| `scripts/deploy.sh`, build pipeline | Solan | |
| Playwright tests, baselines | Kade Vox + @copilot | Kade Vox sets strategy |
| `terraform/` changes | Myrren + Stratia | |
| Hugo local dev environment | Orin | Version conflicts, module issues |
| Content Markdown edits | @copilot | Surgical; preserve front matter |
| New services/offering pages | @copilot | Follow existing page structure |

## Do Not Route to @copilot Without Review
- Changes to `themes/` (submodule — do not touch)
- IAM or bucket policy changes
- CloudFront origin / behavior restructuring
- WebGL scene additions
