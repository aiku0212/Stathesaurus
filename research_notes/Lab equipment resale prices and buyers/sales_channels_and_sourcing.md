# Sales Channels, Buyer Requirements, Automation Limits, and Sourcing Access for a Small Boston Used-Lab-Equipment Reseller (as of Oct 2026)

Research note: Many primary sites (ebay.com, equipnet.com, ssllc.com) gave DNS errors from this environment, so WebFetch failed on them. Most findings below come from WebSearch snippets and from secondary sources such as trade press, university PDFs and aggregators. Dates are marked where sources are older. Anything without a citation is in Inferences or Gaps.

## 1. Marketplaces (eBay, LabX, Kurtzy, consignment, DOTmed, Facebook/Craigslist, Amazon Business)

### Takeaway
eBay is the most accessible channel for parcel-sized items, and its official Sell APIs allow listing automation. Since Feb 20, 2026, its User Agreement explicitly bans AI "buy-for-me" agents and AI/LLM scraping, so automation is limited to the seller side and approved APIs. Neither LabX nor Kurtzy fee schedules could be confirmed. Consignment houses (BioSurplus, EquipNet) take roughly 15–20%. DOTmed suits clinical items and offers a free 30-listing tier.

### Cited Findings
**eBay: the 2026 AI-agent and scraping ban**
- eBay posted a User Agreement update on Jan 20, 2026, effective Feb 20, 2026. It bans "buy-for-me" agents, LLM-driven bots and automated flows that place orders without human review, unless eBay approves them — [Value Added Resource](https://www.valueaddedresource.net/ebay-bans-ai-agents-updates-arbitration-user-agreement-feb-2026/); [EcommerceBytes](https://www.ecommercebytes.com/2026/01/21/ebay-bans-ai-shopping-agents-updates-arbitration-provision/); [The Register](https://www.theregister.com/2026/01/22/ebay_updates_legalese_to_ban/)
- The anti-scraping clause ("any robot, spider, scraper, data mining tools…") now explicitly covers bots used for AI or LLMs. eBay's robots.txt also blocks several AI crawlers, reportedly including Anthropic's and Perplexity's — [TechSpot](https://www.techspot.com/news/111046-ebay-banning-agentic-ai-shopping-though-could-activate.html); [Shopifreaks](https://www.shopifreaks.com/ebay-bans-unapproved-agentic-shopping-bots-from-its-platform-set-stage-for-more-partnerships/). Reports conflict on whether Google's shopping bot is exempt.
- A further agreement revision is dated May 27, 2026; its details were not verified — [ConductAtlas](https://conductatlas.com/platform/ebay/ebay-user-agreement/provision/CA-P-035187/prohibition-on-automated-scraping-and-bot-access/)

**eBay: fees**
- eBay's help page says certain Business & Industrial "Capital Equipment" categories have their own final value fee, listed on the eBay.com fees page — [eBay help (contextual FVF)](https://pages.ebay.com/ebaymotors/help/sell/contextual/final-value-fees.html)
- Third-party guides give a 2026 standard FVF of about 13.6% up to $7,500 and 2.35% above that. The per-order fee is $0.30 for orders of $10 or less and $0.40 above $10 — [Taxomate](https://taxomate.com/blog/ebay-seller-fees); [underpriced.app](https://underpriced.app/blog/ebay-seller-fees-2026). One undated source lists Business & Industrial at 4.35%, which may be stale — [eDesk](https://www.edesk.com/blog/how-much-ebay-take-per-sale/). No source confirmed the exact rate for Healthcare, Lab & Dental.

**eBay: developer/API access**
- eBay's Application Growth Check is free. It is required to raise daily API call limits, to access restricted APIs in production and to get extra keysets, and it requires a working, testable app that complies with the API License Agreement — [eBay Developers: Growth Check](https://developer.ebay.com/api-docs/static/gs_request-an-application-growth.html); [KB 5196](https://developer.ebay.com/support/kb-article?KBid=5196)
- eBay's developer program page notes an updated API License Agreement with "important restrictions applied to the use of Restricted APIs and AI content" — [eBay Developers KB](https://developer.ebay.com/support/knowledge-base/5196)

**LabX**
- LabX is an independent marketplace that does not sell or ship items itself; sellers manage each sale. Buyer guides mention PayPal, Escrow.com and ProPay as payment options — [Excedr](https://www.excedr.com/blog/buying-lab-equipment-through-labx-read-this-first)
- Third-party Apify scrapers exist for LabX — [Apify](https://apify.com/crawloop/labx-scraper). They are unofficial, and whether they comply with LabX's terms is unknown.

**BioSurplus / EquipNet consignment**
- In BioSurplus's consignment model, the consignor owns the item until it sells. Items ship to BioSurplus storage at the consignor's expense, or stay on site and ship at the buyer's expense. The seller must clean and decommission the item and complete a decontamination certificate — [Lab Manager](https://www.labmanager.com/consignment-can-maximize-returns-on-pre-owned-lab-equipment-23761)
- EquipNet's individual-asset sales charge a seller's premium of 15% for exclusive listings and 20% for non-exclusive — [EquipNet individual asset sales](https://www.equipnet.com/investment-recovery-solutions/individual-asset-sales/)

**DOTmed (clinical/medical items)**
- The free tier allows 30 equipment listings; paid upgrades run about $40–$350/month (top tier 600 listings). Self-managed auctions carry a setup fee plus 2–5% commission. When DOTmed handles payment, seller fees are 15–20%, by page. Buy Now carries no DOTmed commission, only PayPal or Stripe fees. Pages vary in age and some are promotional — [DOTmed upgrades](https://www.dotmed.com/users/my/newupgrades.html?lang=en); [DOTmed self auctions](https://dotmed.com/features/auctions_self.html); [DOTmed vs eBay](https://www.dotmed.com/marketing/ebay.html)

**Facebook Marketplace**
- Secondhand guides say Meta's Commerce Policies prohibit medical devices, items that diagnose or treat, and hazardous, flammable, toxic or radioactive materials. Automated moderation sometimes removes legitimate listings — [Vendoo](https://blog.vendoo.co/reseller-guide-to-facebook-marketplace-prohibited-items); [OneShop](https://oneshop.com/blog/facebook-marketplace-prohibited-items)

**Other niche marketplaces (comparison)**
- Lab Merchant charges a flat fee for a 90-day classified ad and takes no commission on sale — [LBIC](https://www.lbic.com/laboratory-equipment)

### Inferences
- On eBay, an AI agent may draft listings, suggest prices from the seller's own sold data (Seller Hub, Terapeak inside the seller's account), and create or revise listings through the Sell Inventory API. It may also pull orders and push tracking through the Fulfillment API. It may not scrape eBay search, run unapproved AI crawlers against eBay, or place bids or purchases.
- For a Healthcare, Lab & Dental item, the FVF is likely at or near the standard ~13.6% unless it falls in a "Capital Equipment" subcategory. The current fee table must be checked by hand.
- Clinical items (patient monitors, ultrasound probes) belong on DOTmed and eBay, not Facebook. Some FDA-regulated devices (e.g., prescription devices) carry eBay restrictions as well; this was not verified.
- Craigslist Boston and Facebook local work best as pickup-only, cash-sale outlets for bulky benchtop items. Fees are minimal; trust and fraud risk are the main costs.

### Gaps
- LabX seller fees and listing packages. No published schedule was found; contact LabX sales.
- Kurtzy fees. No search result mentioned Kurtzy at all, so it may be small or renamed. Verify it exists before relying on it.
- BioSurplus consignment split was not published.
- Amazon Business restrictions for used lab or medical items. Not researched successfully; Amazon gates many scientific and medical categories and generally restricts "used" condition. Treat as low-feasibility until checked.
- r/labrats rules on selling: the subreddit rules page was not retrievable. A thread shows some buyers use eBay with reimbursement because university cards can't be used there — [r/labrats mirror](https://cal1.lr.ggtyler.dev/r/labrats/comments/1jrg1wr/lab_equipment_on_ebay). Assume no commercial posts without mod permission.
- Scientific Bioprocessing or other dealer "we buy" program terms were not found.

## 2. Direct-to-lab channels (university reuse, incubators, communities)

### Takeaway
Boston university reuse systems are mostly internal: BU sends surplus to other departments first and restricts outside sales. Incubators like LabCentral already supply shared common equipment. Their resident startups are still a realistic niche for specialized or backup gear, but no public vendor channel or Slack was found.

### Cited Findings
- BU procedure: surplus moveable capital equipment (≥$5,000 cost, ≥1-year useful life) is offered to other BU departments first through a "Not in Use" file. Sales to outside parties need written approval from a dean, chair or unit head, are "as is", and come with a bill of sale recording model and serial numbers — [BU Research Procedure](https://www.bu.edu/research/forms-policies/sale-of-moveable-capital-equipment-procedure-for-the/); [BU Sell Equipment](https://www.bu.edu/cfo/comptroller/departments/rfo/property/sell-equipment)
- BUMC Equipment Exchange lists surplus research equipment and supplies for the BU research community, not the public — [BUMC Equipment Exchange](https://www.bumc.bu.edu/camed/research-impact/research-resources/bumc-equipment-exchange)
- LabCentral provides "all reasonably common lab equipment" to residents, valued at more than $7M (later figure; $3M in 2014). It hosts up to roughly 125 startups (75 in an earlier source; 30 in 2014). Vendor partnerships happen through its networks (e.g., Eppendorf, Thermo Fisher) — [LabCentral case study](https://www.labcentral.org/case-studies/satellite-bio-case-study); [LabCentral 2014 report](https://portal.labcentral.org/uploads/assets/Impact_Report_2014.pdf); [Thermo Fisher](https://www.thermofisher.cn/cn/en/home/brands/inspire/keep-seeking/meet-innovators/collaboration-in-science.html?icid=8)

### Inferences
- A BU student can watch BUMC Equipment Exchange and BU property listings for sourcing. The procedure suggests buying as an outside party requires department approval, and the student-employee conflict of interest should be cleared with BU first.
- The best direct-sale targets are lab managers and ops leads at seed-stage startups in BioLabs, LabCentral, Harvard Innovation Labs and similar spaces, plus core facility managers needing spares. Contact through LinkedIn or warm intros, with one-to-one personalized emails. An AI agent can draft and research outreach, but a human should send each message, follow CAN-SPAM, and avoid bulk scraped lists.

### Gaps
- Harvard and MIT surplus or reuse programs (public access and terms) were not retrieved.
- No source on LabCentral, BioLabs or Harvard i-lab Slack communities or their vendor-solicitation rules. Likely resident-only.
- No Boston Discord or Slack lab-equipment swap community was found.

## 3. Selling wholesale to dealers or refurbishers (exit channel)

### Takeaway
Dealers and liquidators (Lab Liquidators, BioSurplus, EquipNet, SSLLC, American Laboratory Trading) buy outright for speed. No source gave the typical fraction of resale paid.

### Cited Findings
- The three exit routes are direct sale to a reseller (fastest), consignment (higher return, slower) and auction — [Lab Manager guide](https://www.labmanager.com/a-guide-to-selling-used-lab-equipment-2022)
- One dealer buys scientific, analytical, vacuum, optics and test equipment. It passes on commodity furniture, hazmat, and items where freight exceeds resale value — [Lab Liquidators](https://labliquidators.com/sell-my-lab-equipment/)
- Lab equipment loses roughly 40–75% of its value over 5 years. Recent HPLC/FPLC systems, sequencers, mass specs and specialist microscopes hold value best — [Lab News](https://labnews.co.uk/unlocking_the_hidden_value_of_your_lab/)

### Inferences
- The 15–20% consignment seller premiums (EquipNet) set a ceiling: outright dealer offers will be well below consignment net. Commonly cited industry practice is 20–40% of expected resale, but that range is unsourced here.

### Gaps
- Typical wholesale-to-resale ratio. Get quotes on specific models.

## 4. What institutional buyers require (invoices, W-9, tax, warranty, decon, PO, net-30)

### Takeaway
Universities can pay individuals and sole proprietors. Harvard's Supplier Portal has an individual registration path with W-9 generation and Zelle payment, and many schools use PaymentWorks with a sole-proprietor option. Buyers will send an ST-5 exemption certificate; the seller must keep it on file. A decontamination certificate is standard. No source gave warranty or net-terms norms for small resellers.

### Cited Findings
- Harvard's Supplier Portal lets US individuals self-register. A valid IRS tax document is required, and the portal can generate a pre-filled W-9 to sign and upload. Zelle is available to individuals with US bank accounts, Paymode-X to companies, and the vendor onboarding team reviews registrations — [Harvard FAS Supplier Portal guide](https://adminops.fas.harvard.edu/files/fasadministrativeoperations/files/harvard_supplier_portal_us_individual_self_guided_registration_0_0.pdf)
- PaymentWorks (used by Ohio U, Penn State, Rutgers and others) has an individual/sole-proprietorship option that generates an electronic W-9. Departments no longer collect W-9s directly — [Penn State](https://procurement.prod.fbweb.psu.edu/research-participant-registration-guide); [Ohio U](https://www.ohio.edu/finance/business-matters/supplier-management-transformation-progress-on-paymentworks-implementation)
- Massachusetts exempt purchasers, including BU, MIT and Tufts, give vendors Form ST-5 (and a 501(c)(3) also needs an ST-2) under MGL c.64H §6(d)/(e). The certificate carries an exemption number and expiration date. Single-purchase certificates need a receipt. Buyers paying with a personal card pay the tax — [BU ST-5](https://www.bu.edu/cfo/files/2024/09/ST-5-Boston-University-Partially-Complete-copy-version-9-6-24.pdf); [MIT ST-5](https://hq.csail.mit.edu/sites/default/files/documents/ST-5%20MIT%20Sales%20Tax%20Exempt%20Form%202024_OpenAI_0.pdf); [Tufts ST-5](https://access.tufts.edu/sites/default/files/finance/Tufts%20University%20ST-5%20Revised%208.30.23.pdf); [GWU MA guidance](https://taxdepartment.gwu.edu/sites/g/files/zaxdzs5981/files/downloads/MASalesTax_0.pdf)
- A university card generally can't be used on eBay, though buyers may get reimbursed — [r/labrats mirror](https://cal1.lr.ggtyler.dev/r/labrats/comments/1jrg1wr/lab_equipment_on_ebay)
- Decontamination certificates are standard in the resale chain. BioSurplus requires one from consignors — [Lab Manager](https://www.labmanager.com/consignment-can-maximize-returns-on-pre-owned-lab-equipment-23761)
- The Massachusetts sales tax rate is 6.25%, as seen on an SSLLC Fall River auction invoice from 2015 — [BidSpotter SSLLC 2015](https://www.bidspotter.com/en-us/auction-catalogues/bscsur/catalogue-id-bscsur10002)

### Inferences
- A seller making regular in-state sales needs a Massachusetts sales tax registration through MassTaxConnect, charges 6.25% unless the buyer supplies an ST-5, and keeps the certificates. eBay collects and remits marketplace tax itself; direct invoices fall on the seller.
- Trust package for institutional buyers: a professional invoice and quote (business name or DBA, EIN optional, though a sole proprietor can use an SSN on the W-9), a signed decontamination certificate, a functional test report with photos or video, serial number, a 30-day DOA/return warranty, and acceptance of PO numbers on invoices. Net-30 means floating capital; with $2,000, keep invoiced sales small or ask for card payment.

### Gaps
- No primary source on BU, MIT or Harvard practice for paying a student-run sole proprietorship (conflict-of-interest rules for BU students selling to BU labs).
- No source on typical warranty lengths (30 vs 90 days) or net-terms norms among small lab resellers.
- MassTaxConnect registration steps were not retrieved.

## 5. What can be automated through official APIs versus human-only

### Takeaway
Seller-side work is the automatable part: eBay Sell APIs (Inventory, Fulfillment) under a registered developer account, the seller's own analytics, drafting, and email drafts. Buying, bidding, scraping marketplaces and auction sites, and mass outreach must not be automated.

### Cited Findings
- eBay prohibits unapproved AI buying agents and AI/LLM scraping (effective Feb 20, 2026) — [Value Added Resource](https://www.valueaddedresource.net/ebay-bans-ai-agents-updates-arbitration-user-agreement-feb-2026/)
- eBay API use is subject to the API License Agreement, newly restricted for "Restricted APIs and AI content". Higher call limits and restricted APIs need a Growth Check — [eBay Developers](https://developer.ebay.com/api-docs/static/gs_request-an-application-growth.html)
- EquipNet registration requires your exact legal name as shown on your W-9 — [EquipNet FAQ](https://www.equipnet.com/faqs/)

### Inferences
- **OK to automate:** listing creation and revision through the Sell Inventory API, order and tracking sync through the Fulfillment API, repricing within the seller's own rules, photo editing, condition write-ups, test-report templates, invoice generation, tax-certificate filing, inventory spreadsheets, calendar reminders for auction close and removal deadlines.
- **Human-only:** every bid and purchase, auction registrations, accepting terms, final pricing approvals, sending outreach messages, handling disputes and returns, decon or test sign-offs.
- **No LabX listing API was found:** assume manual posting.

### Gaps
- Whether LabX offers bulk upload or an API.
- Current text of eBay's API License Agreement AI clause.

## 6. Sourcing: registering and bidding at lab-equipment auctions (SSLLC, EquipNet, BioSurplus, Heritage/Federal, BidSpotter/HiBid, GovDeals)

### Takeaway
Buyer's premiums at lab-equipment auctions run about 15–19%, and Massachusetts adds 6.25% tax unless you hold a resale certificate. Removal windows are short (often 5 business days to pay, about 10 to remove), which matters without a truck. No specific fall 2026 Boston auction calendar could be confirmed.

### Cited Findings
- **SSLLC:** bidders create an account on SSLLC's own auction platform, and the auctioneer approves each registration. Terms vary by sale and are set out in a separate Auction Terms of Use — [SSLLC Auctions blog](https://ssllc.com/about-us/blog/SSLLC-Auctions); [SSLLC Terms](https://ssllc.com/terms-and-conditions/)
- An SSLLC Fall River, MA BidSpotter sale (Feb 2015) charged a 15% buyer's premium plus 6.25% sales tax — [BidSpotter](https://www.bidspotter.com/en-us/auction-catalogues/bscsur/catalogue-id-bscsur10002). Other BidSpotter medical sales show 18% — [BidSpotter medical](https://www.bidspotter.com/en-us/for-sale/laboratory-and-pharmaceutical-equipment/medical-equipment)
- **EquipNet:** register under your W-9 name. Payment by EFT preferred; checks are accepted, with a 4-business-day hold before release, and Visa, MC and Discover for US invoices — [EquipNet FAQ](https://www.equipnet.com/faqs/). Search snippets showed EquipNet Massachusetts lab lots closing in May 2026.
- **Heritage Global / Federal Equipment:** a Framingham, MA lab sale (Dec 2023) and a Hayward, CA sale (Sept 2025) both charged a 19% buyer's premium. Heritage and American Laboratory Trading ran the Rubius Therapeutics Cambridge auction (Jan 2023) — [Federal Equipment blog](https://fedequipblog.fedequip.com/lab-biopharma-equipment-auction/); [Federal Equipment Apertor](https://fedequipblog.fedequip.com/late-model-lab-equipment-auction-assets-formerly-of-apertor/); [HGP Rubius](https://www.hgpauction.com/lab-equipment-from-rubius-therapeutics/)
- **BidSpotter** lists hundreds of Massachusetts lab and pharma lots (462 at time of indexing) — [BidSpotter lab](https://www.bidspotter.com/en-us/for-sale/laboratory-and-pharmaceutical-equipment). BidSpotter and Proxibid share a parent (ATG) — [govauctions.app](https://govauctions.app/guides/auction-aggregator-landscape). HiBid Massachusetts landing page — [HiBid MA](https://massachusetts.hibid.com/)
- **GovDeals:** terms are set per selling agency. Typical examples: pay within 5 business days, remove within 10 business days of the Buyer's Certificate, and a defaulting buyer can be barred — [Cabarrus County](https://docs.cabarruscounty.us/WebLink/1/doc/1617374/Page109.aspx); [City of Bryan](https://www.cityofbryan.net/?p=4379). An aggregator says the median government medical/scientific lot sells for about $78 and premiums are often around 10% — [govauctions.app](https://govauctions.app/sold-prices/medical-scientific)
- **BioSurplus** has relaunched ("BioSurplus Returns!") and is buying and accepting consignments; the press release is undated — [StreetInsider](https://www.streetinsider.com/Business+Wire/BioSurplus+Returns%21/26857491.html)

### Inferences
- With no truck and $2,000 in capital, filter for small lots (pipettes, small centrifuges, pumps, power supplies, optics) and budget hammer price × ~1.19 × 1.0625, plus packing and shipping, as all-in cost. A Massachusetts resale certificate (Form ST-4) can avoid the 6.25% tax on items bought for resale, but this was not verified for each auctioneer.
- Use auctioneers' optional shipping or third-party pack-and-ship services (e.g., local UPS Store packers), or rent a Zipcar or U-Haul van for the removal day.
- An AI agent may track public calendars by hand-checked links or email alerts (subscribe to SSLLC, EquipNet, Federal Equipment and BidSpotter newsletters), compute max bids and set reminders. A human places each bid.

### Gaps
- No confirmed list of Boston-area lab auctions for Oct–Dec 2026 (sites unreachable; search found none). Subscribe to auctioneer email lists.
- Exact current buyer's premiums for SSLLC, EquipNet and GovDeals; deposit requirements (many ATG auctioneers place card holds, unverified); inspection-day norms.
- Whether EquipNet or SSLLC accept individual (non-company) bidders without a business entity. EquipNet's FAQ implies a company or W-9 name suffices.
