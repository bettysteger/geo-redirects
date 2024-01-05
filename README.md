# Redirect by country or language

For large multi-regional or multi-lingual sites, you may want to send site visitors to different content based on their location (by country GeoIP data) or their browser’s language configuration.

[Netlify](
https://docs.netlify.com/routing/redirects/) can handle these requests with GeoIP- and language-based redirects directly from their CDN nodes.

When you add these redirect rules, Netlify automatically creates alternate headers to enable the redirection in our CDN nodes. This removes the need for a round trip to our origin servers and ensures that normal pages, besides country or language based redirects, are cached on the CDN nodes.

Here are some examples: https://github.com/bettysteger/geo-redirects/blob/main/_redirects

The `Country` attribute accepts [ISO 3166 country codes](http://dev.maxmind.com/geoip/legacy/codes/iso3166/).

The `Language` attribute accepts [standard browser language identification codes](http://www.metamodpro.com/browser-language-codes).

## Affiliate Link Examples

https://302.netlify.app/flaconi should redirect to flaconi.at if you are in Austria, otherwise it should redirect to flaconi.de. 
