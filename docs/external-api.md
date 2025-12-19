# External API — TVmaze

This project uses the public TVmaze REST API to obtain show and episode information.

Overview

- Base URL: https://api.tvmaze.com
- Type: public REST API that returns JSON and supports HAL/HATEOAS-style embedding.

Common endpoints used by NextWatch

- Search shows: `/search/shows?q=:query` — fuzzy search to find shows by name.
- Single show: `/shows/:id` — main show data; supports `?embed=` to include related resources (episodes, cast, etc.).
- Show episodes: `/shows/:id/episodes` — full episode list for a show.
- Episode detail: `/episodes/:id` — single episode information.

Important notes

- Embedding: use `?embed=` or `embed[]=` to request related resources in the same response (reduces extra requests).
- Rate limiting: TVmaze allows at least ~20 calls per 10 seconds per IP; handle `429` gracefully (backoff/retry).
- Caching: TVmaze responses are cached for ~60 minutes at the edge. Cache images on your side for performance.
- CORS & HTTPS: endpoints are HTTPS and CORS-enabled — safe to call from the browser.
- Licensing: TVmaze data is CC BY-SA — attribute TVmaze when showing data sourced from the API.

How NextWatch integrates

- The frontend uses the client in `lib/apis/tvmaze-api.ts` to search shows and fetch show/episode details.
- Configure the API base URL with the `NEXT_PUBLIC_TVMAZE_API` environment variable (defaults to `https://api.tvmaze.com`).

Examples

- Search: `https://api.tvmaze.com/search/shows?q=girls`
- Show with embedded episodes: `https://api.tvmaze.com/shows/1?embed=episodes`

References

- TVmaze API docs: https://www.tvmaze.com/api
