# AI Link Opportunity Studio

Built by SEO Girl - Ami. A standalone AI-assisted workspace for backlink prospect research, guest-post pitches, digital PR plans and blog drafts.

## Run locally
Open index.html in a browser. Internet access is needed for Gemini generation. Select **Load demo workspace** to explore fictional sample data and prepared drafts.

## Deploy to Vercel
1. Upload index.html, vercel.json and this README to the root of your GitHub repository.
2. Import the repository into Vercel.
3. Select the Other framework preset. Leave the build command unset and use the repository root as the output directory.
4. Deploy and test Generate with Gemini on the live URL.

No dependency installation or build is required.

## AI connection
The app calls https://gemini-proxy-boldstudio.vercel.app/api/gemini using the gemini-3.8-flash model. The GEMINI_API_KEY belongs in the existing proxy project's server-side Vercel environment variables, not this app or the GitHub repository. This app needs no API key environment variable while using that proxy. Generation depends on proxy availability, access settings, CORS and Gemini quota. This package does not change proxy authentication or rate limits.

## Features
- Local CSV prospect import and transparent topic overlap
- Backlink outreach, guest-post pitching and digital PR planning
- Editable blog drafts and source/proposed-link lists
- Copy-and-links downloads and a local outreach tracker
- Fictional demo prospects and prepared examples

## Data and limitations
CSV data is parsed in your browser. When you select Generate, the current brand brief, selected prospect and supplied sources are sent through the Gemini proxy. No URLs are crawled and no emails are sent. Demo links on example.com are placeholders, not real placements. AI output needs human fact-checking and editorial review. Local saves use browser storage; export backups. There are no measured time-saving or link-acquisition claims.

## Validation
Automated checks covered CSV parsing, URL validation, demo modes, mocked AI success/error handling, export context and tracker attribution. The proxy previously returned a real successful Gemini response during app development. Browser visual QA and this app's Vercel deployment have not been verified.

## Unlinked brand mentions
Open Brand mentions to load fictional demo coverage or import a mention CSV. Required columns: URL, Title, Excerpt, Link status (unlinked, linked or unknown). Optional: Contact URL. Gemini assesses up to 30 mentions and drafts outreach for relevant user-marked unlinked coverage. No web search or link crawling occurs; verify current status before outreach. Download the analysis with its source snapshot.

## Broken links
Open Broken links to load fictional demo references or import a CSV. Required: Source URL, Broken URL, Anchor, Status. Status values: reported, verified broken, working, unknown. Optional: Notes, Checked date, Contact URL. Add a replacement URL and verified contents. Gemini assesses up to 30 references and prepares a replacement plan and outreach for relevant user-verified broken links. No crawling or HTTP checks occur. Recheck status and suitability before outreach. Working links are excluded; uncertain statuses need verification. Export preserves the source snapshot.

## Linkable Asset Planner
Open Asset planner to load fictional expertise and source notes or describe your own material. Gemini compares asset concepts and prepares a production brief with evidence requirements and review gates. Download the plan with its original input notes, or send it to the content studio as draft context. Research, implementation, verification and publication remain human work. No backlink outcomes or time savings are promised.
