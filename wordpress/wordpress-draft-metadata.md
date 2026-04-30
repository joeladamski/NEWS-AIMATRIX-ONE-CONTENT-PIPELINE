# WordPress Draft Metadata Standard

## Required Front Matter Fields
Each article must provide the following metadata before WordPress draft creation:

- `article_id`: Stable internal ID (`ART-YYYY-NNNN` suggested)
- `title`: Human-readable article title
- `slug`: URL slug candidate
- `status`: Repository workflow status
- `canonical_url`: Canonical URL or placeholder
- `excerpt`: Short summary for WordPress excerpt
- `seo_title`: Search title
- `seo_description`: Search description
- `seo_keywords`: List of target keywords
- `wp_categories`: List of WordPress category slugs
- `wp_tags`: List of WordPress tag slugs
- `review_owner`: Human reviewer/owner
- `approved_by`: Human approver (required before draft push)
- `approved_utc`: UTC timestamp of approval

## SEO Fields Rules
- `seo_title`: 50-60 characters target.
- `seo_description`: 140-160 characters target.
- `seo_keywords`: 3-8 focused terms, no keyword stuffing.
- `excerpt`: 1-2 concise sentences aligned to article intent.

## Canonical URL Placeholder Rules
Allowed values:
- Real URL (preferred at approval stage), e.g. `https://news.aimatrix.one/example-slug`
- Placeholder: `TBD_CANONICAL_URL`

Rules:
- Placeholder is allowed in draft/review states.
- Human reviewer must confirm placeholder acceptability before WordPress draft push.
- Do not use fake domains or non-governed URL patterns.

## WordPress Taxonomy Mapping Rules
- `wp_categories` must use category slugs defined in `wordpress/category-map.md`.
- `wp_tags` must use tag slugs defined in `wordpress/tag-map.md`.
- If no approved mapping exists, stop and request human taxonomy decision.

## WordPress Post Status Rule
All WordPress creations from this repository must set:
- `post_status: draft`

No other WordPress post status is permitted through this operational standard.
