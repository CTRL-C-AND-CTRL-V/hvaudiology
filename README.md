# Hunter Valley Audiology: website rebuild (demo)

A static HTML/CSS demo of the rebuilt hvaudiology.com.au, for client review. There is no JavaScript, backend or build step.

- Content source: [hvaudiology-site-inventory.md](hvaudiology-site-inventory.md)
- Visual system: [DESIGN.md](DESIGN.md)

## Viewing it

Open `index.html` in a browser. All links are relative, so the site works straight from disk and from any host or sub-path. To share it with the client, deploy the folder as-is to Netlify, Cloudflare Pages or GitHub Pages. Every page has `noindex`, so the demo can't compete with the live site in search results.

## Structure

```
index.html                 Home
about/  services/  contact/  booking/  hearing-test/  blog/
service/<slug>/            9 service pages (same URLs as the WordPress site)
hearing/                   Hearing health hub + 4 guides
blog/ear-wax-and-hearing-aids/   Article template
contact/thank-you/         Form confirmation
404.html
assets/css/site.css        Entry point; imports the layers below in order
  tokens.css               Design tokens from DESIGN.md (names match its Tailwind @theme block)
  base.css                 Reset, element defaults, type roles (.display, .h2, .lead, .label)
  layout.css               .container, .section, .split, .article-layout
  components.css           One block per future component, BEM-named
  pages.css                Page-only styles (home hero etc.)
  utilities.css            Last layer; always wins
_redirects                 Old-URL redirects for launch
```

## Conventions that make the production move straightforward

- **URLs match the current site** (`/service/…`, `/hearing/…`), so search rankings carry over. The one exception is the misspelled "anotomy" page, which `_redirects` handles.
- **Partials are marked.** Header and footer are repeated in every page between `<!-- partial: … -->` comments. Each becomes one layout component.
- **Integration points are marked.** Every place a live system plugs in carries `data-integration="…"` and a comment:

  | `data-integration` | Page | Production system |
  |---|---|---|
  | `booking` | /booking/ | Hearing Health Portal widget, or a custom booking service |
  | `enquiry` | Home, /contact/ | Form endpoint (`/api/enquiries`) + spam protection + email to clinic |
  | `newsletter` | Footer | Mailing list provider (`/api/newsletter`) |
  | `google-reviews` | Home | Google Business Profile reviews |
  | `hearing-screener` | /hearing-test/ | Beyond Hearing screener (currently opens externally) |
  | `map` | /contact/ | Google Maps Embed API |
  | `cms-posts` | /blog/ | CMS posts collection with pagination and topics |

  Form field names (`name`, `phone`, `email`, `clinic`, `message`) are meant to be the API contract.
- **Demo-only content is marked.** Search for `demo-note` and `Photo:` placeholders (`.media`) to find everything to replace before launch. Delete the "Demo build" line in the footer and the `noindex` meta at launch.
- **CSS uses cascade layers and tokens only.** Components never use raw hex values, so they port directly to Tailwind or CSS modules.

## Suggested production path

1. **Framework:** Astro (mostly static content, ships little JS) or Next.js. Turn each partial and component block into a component, and each folder into a route.
2. **Content:** Put services, hearing guides and the 27 blog posts in a headless CMS so the clinic can edit them. The existing WordPress install could also serve as a headless CMS through its REST API.
3. **Integrations:** Replace each `data-integration` slot using the table above.
4. **Launch:** Point the domain, add `_redirects`, remove `noindex` and the demo notes, and submit the sitemap.

## Needed from the client

- Opening hours for both clinics
- Is (02) 9184 9628 a phone line or a fax? The demo labels it "Landline".
- Photos (every `Photo:` placeholder says what's needed), plus the logo files
- Jai's LinkedIn URL
- Licence to reuse Unitron campaign imagery, if wanted
- Review of the draft copy on the service and hearing health pages
