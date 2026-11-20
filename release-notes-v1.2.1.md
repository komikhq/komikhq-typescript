## What's Changed in v1.2.1

### 🚀 Restored Admin Chapter Lifecycle & Binary Uploads
- `adminInitializeChapter`: Initialize new chapters with auto-generated slugs.
- `adminUploadChapterPage`: Upload single page images directly via R2 multipart form-data.
- `adminFinalizeChapter`: Finalize chapter page counts and recalculate total comic chapter numbers.
- `adminUpdateChapter`: Partial update for chapter details (number, title, access tier, early access).
- `adminListChapters`: List all chapters for a given comic sorted by chapter number.

### 🖼️ Multipart Comic Creation & Updates
- `adminCreateComic`: Full multipart form-data support for direct binary uploads of cover and banner images alongside JSON/URL sources.
- `adminUpdateComic`: Multipart form-data support for updating comic cover and banner images.

### 🗺️ Multi-Feed Sitemap APIs
- `getSitemapSummary`: Metadata summary of the catalog (latest update timestamps & total counts).
- `listSitemapComics`: JSON feed of indexed comics with pagination and limits.
- `listSitemapChapters`: Paginated JSON feed of comic chapters joined with comic slugs.
- `getComicsSitemapXml`: Pure XML sitemap feed with JSON negotiation support (`?format=json`).
- `getChaptersSitemapXml`: Pure XML sitemap feed with JSON negotiation support (`?format=json`).

### 📦 Distribution
- Package: `@komikhq/komikhq-typescript`
- Version: `1.2.1`
