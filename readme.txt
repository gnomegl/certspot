certspot
--------
certificate transparency search for domains and subdomains.
uses the certspotter (sslmate) api.

install
  basher install gnomegl/certspot

usage
  certspot example.com

options
  -l, --limit     max results to return
  -j, --json      raw ndjson output
  -q, --quiet     suppress color/progress
  --no-header     skip header
  --csv           csv output
  --sort-date     sort by first_seen (newest first)
  --no-cache      skip cache, force fresh api call
  --max-age       cache ttl in hours (default: 24)

environment
  CERTSPOTTER_API_KEY   api key for unlimited access
                        get one at: https://sslmate.com/signup?for=ct_search_api

rate limits
  free tier: ~1 req per 3 min, 100 certs max per query
  with api key: unlimited requests, full pagination
  results cached for 24h in ~/.cache/certspot/

requires
  curl, jq
