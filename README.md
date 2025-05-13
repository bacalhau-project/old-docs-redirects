# Bacalhau Documentation Redirects

This repository handles redirects from docs.bacalahau.org to the new documentation on bacalhau.org. It's deployed using Netlify for simple maintenance and high reliability.

## Adding New Redirects

To add a new redirect:

1. Edit the `_redirects` file
2. Add your redirect in the appropriate section
3. Use this format:

```
/old-path    https://bacalhau.org/new-path    301
```

With wildcards:

```
/old-section/*    https://bacalhau.org/new-section/:splat    301
```

**Important**: More specific paths should come before wildcards.

## Deployment

Just push changes to the main branch - Netlify will automatically deploy the updates.

## Gitbook Broken Links

The "Gitbooks Broken Links" section contains redirects for URLs identified from Gitbook's analytics, filtered to exclude bot traffic by removing "unknown browsers" from the statistics.

## Testing Your Changes

After deploying:
1. Visit the old URL at docs.bacalahau.org/your-path
2. Confirm it redirects to the correct location