# Public-Data and Information-Arbitrage Products an AI Agent Could Run for Underserved Groups (as of October 2026)

Research notes for a 21+ BU student in Massachusetts (psychology research, statistics, life-sciences consulting background; low capital). Research method: web search plus fetches of reachable pages. Several official sites were unreachable from this environment (DNS failures on malegislature.gov, open.gsa.gov, clinicaltrials.gov, open.fda.gov, dev.to), so some API and statute details come from secondary sources and are flagged as such. The session's web-search budget ran out before CAN-SPAM and FCRA could be researched; see Gaps.

Candidates evaluated (ranked by overall attractiveness, details in Key Question 1 Inferences):
1. Trade-specific Massachusetts public-bid digest for micro-businesses (strongest)
2. Local / niche small-nonprofit grant-deadline digest
3. Condition-specific clinical-trial alerts distributed through patient groups (best fit for the user's background)
4. Multi-city Massachusetts affordable-housing lottery and waitlist alerts (high benefit, weak monetization; sponsor-funded only)
5. Trade-specific building-permit lead alerts from municipal open data (medium; one predatory variant to avoid)
6. Drug-shortage / discontinuation alerts (low to medium; better as a feature of #3)
7. Class-action settlement eligibility alerts (saturated; predatory patterns common)
8. Massachusetts unclaimed-property finder (avoid the finder-fee model; benign B2B variant only)
9. Narrow-demographic scholarship alerts (avoid charging students; B2B or sponsor only)

---

## Q1. Which data-to-alert niches are genuinely under-served as of 2026?

### Takeaway
The raw-data layer is largely commoditized: there are cheap Apify scrapers for SAM.gov, Grants.gov, building permits, openFDA shortages and ClinicalTrials.gov. The real gaps are curation, localization and distribution to small buyers. The clearest under-served niches are (a) Massachusetts municipal and state bids triaged by trade for micro-businesses, including SBPP preference flags, (b) local and niche grant deadlines for nonprofits too small for Instrumentl, and (c) non-cancer, condition-specific trial alerts delivered through patient organizations. Housing-lottery alerts have a real coordination gap across municipalities, but residents should not be charged for them.

### Cited Findings
**Procurement (Massachusetts)**
- COMMBUYS offers a free Seller account with automated email notifications, and an active Seller account is required to respond to bids. — [Mass.gov required specifications](https://www.mass.gov/doc/g-required-specs/download)
- COMMBUYS buyers can notify all registered vendors who have designated matching UNSPSC codes, so whether a vendor gets alerts depends on the vendor maintaining its codes correctly. — [Mass.gov: How to add bidder notification](https://www.mass.gov/doc/how-to-add-bidder-notification-to-a-bid-posting/download)
- Municipal bids are scattered. New Bedford says all its public bids are posted on COMMBUYS, that it uses BidNet Direct as its electronic bidding platform, and that its bids also run in the Goods and Services Bulletin and Central Register, which are available by subscription through the Secretary of State's office. — [New Bedford Purchasing FAQ](https://www.newbedford-ma.gov/purchasing/?p=20)
- Central Register and Goods and Services Bulletin ads are submitted online to the Secretary of State's office, separately from COMMBUYS postings. — [MA OIG procurement charts, July 2025](https://www.mass.gov/doc/oig-charts-on-procurement-procedures-july-2025/download)
- Small Business Purchasing Program (SBPP): eligible firms have their principal place of business in MA, at least one year in operation, 50 or fewer FTEs and three-year average gross revenue of $15M or less. Registration is free via the Supplier Diversity Office portal. — [Mass.gov SBPP](https://www.mass.gov/service-details/learn-about-small-business-purchasing-program-sbpp); [SBPP info sheet](https://www.mass.gov/doc/sbpp-information-sheet/download)
- For "Small Procurements" (estimated annual value of $250,000 or less), the award must go to an SBPP participant if an SBPP-eligible response meets best-value criteria, and non-SBPP bids are not evaluated unless no SBPP bidder qualifies. The program covers executive agencies plus voluntary participants and excludes construction and non-recurring purchases under $10K. — [SBPP RFR template language](https://www.mass.gov/doc/small-business-purchasing-program-sbpp-rfr-template-language-0/download)
- A GovSpend presentation lists common bidder complaints, including "very niche product or service offerings" and "set-asides or certifications I don't have". This suggests generic feeds serve niche or certified micro-vendors poorly. — [GovSpend PDF, Sept 2024](https://govspend.com/govspend/wp-content/uploads/2024/09/Uncovering-Quality-Opportunities-in-GovSpend-Bids.pdf)

**Grants**
- Instrumentl's cheapest plan is $299/mo billed annually ($349/mo monthly), which prices out very small nonprofits. — [aitoolsbakery](https://aitoolsbakery.com/blog/instrumentl-pricing/); [grantsights](https://grantsights.com/blog/instrumentl-pricing)

**Clinical trials**
- NIH's TrialGPT (NLM/NCI), an LLM that matches patient summaries to ClinicalTrials.gov trials, is "currently only available as a research prototype" for clinicians, not a patient-facing app. — [FedScoop](https://fedscoop.com/how-nihs-national-library-of-medicine-is-testing-ai-to-match-patients-to-clinical-trials/); [NIH news release](https://www.nih.gov/news-events/news-releases/nih-developed-ai-algorithm-matches-potential-volunteers-clinical-trials)
- In a small pilot (2 clinicians, 6 patient summaries), clinicians using TrialGPT spent about 40% less screening time at the same accuracy. NCI reports 42.6%. — [NIH](https://www.nih.gov/news-events/news-releases/nih-developed-ai-algorithm-matches-potential-volunteers-clinical-trials); [NCI CBIIT, 2024](https://www.cancer.gov/about-nci/organization/cbiit/news-events/news/2024/large-language-models-help-match-patients-clinical-trials)
- Cancer trial-matching services were already numerous in 2018, ranging from minimal-input (diagnosis plus ZIP) to detailed eligibility assessment. This suggests oncology is the most crowded condition area (older source). — [ACS CAN whitepaper, May 2018](https://www.fightcancer.org/sites/default/files/CT_MatchingServicesWhitepaper_ACSCAN_May2018Web_0.pdf)

**Housing**
- Boston's Metrolist offers email notifications for upcoming lotteries and a weekly email of new properties accepting applications. It does not list subsidized housing, public housing or listings outside the Boston MSA. — [Boston Metrolist](https://www.boston.gov/metrolist)
- Other cities run separate processes. Somerville's Inclusionary Housing Program has its own multilingual applications, residency/work preferences and virtual lottery draws (2019–2022 articles). — [Somerville Times](https://www.thesomervilletimes.com/?p=92888); [City of Somerville](https://www.somervillema.gov/news/two-affordable-homeownership-opportunities-somerville-411-432-norfolk-st)
- Town housing pages advise residents to sign up for alerts on multiple state websites. — [Needham: How to Find Affordable Housing](https://needhamma.gov/5674/How-To-Find-Affordable-Housing)
- "Boston Home" lotteries need pre-qualification: apply once to be entered into all Boston Home lotteries. Resales of income-restricted condos are handled outside the lottery system. — [Harvard FCU homebuyer presentation, Feb 2026](https://harvardfcu.org/wp-content/uploads/2026/02/Harvard-FCU_HBFday3_Affordable.pdf)

**Commoditized raw data (evidence that scraping alone is not a moat)**
- Apify hosts many ready-made actors: a US RFP monitor (SAM.gov plus state portals with NAICS/keyword matching), a Boston permits scraper, building-permit scrapers priced from $30 per 1,000 results, and multiple openFDA drug-shortage trackers. — [Apify US RFP monitor](https://apify.com/lowlanddata/us-rfp-monitor.md); [Apify Boston permits](https://apify.com/quarterly_jingo/boston-permits-scraper.md); [Apify building permits](https://apify.com/4l3c/building-permits-scraper); [Apify FDA shortages](https://apify.com/compute-edge/fda-drug-shortages-scraper)

### Inferences
These scorecards are my synthesis. Revenue paths are arithmetic, not observed results.

#### 1. Massachusetts trade-specific public-bid digest for micro-businesses (Rank 1)
- **Data:** COMMBUYS open bids (public search), municipal purchasing pages for MA towns, BidNet-hosted municipal bids, the Secretary of State's Central Register / Goods and Services Bulletin (subscription), and SAM.gov for federal set-asides in MA.
- **Group and benefit:** sole proprietors and firms under 10 employees in one trade, such as snow and ice removal, landscaping, janitorial, interpreting and translation, moving, small IT and AV, catering, or printing. Many qualify for SBPP and Supplier Diversity Office (MBE/WBE/VBE) preferences without knowing which bids carry them. The benefit is not missing $10K–$250K bids that favor them, plus plain-language summaries of requirements (bonding, insurance, prevailing wage, pre-bid meetings).
- **Who pays:** the business, at $19–$49/mo. Alternatives are a B2B white-label deal with a trade association, chamber, Small Business Development Center or minority business organization, or a sponsor such as a local bank or surety/insurance broker (disclosed).
- **Path to $500–$1,000/mo:** 20–30 subscribers at $29, or 10–12 at $79 for a multi-trade or multi-region tier, or one or two association white-label deals at $300–$500/mo.
- **Agent workflow:**
  1. Poll sources daily.
  2. Dedupe across COMMBUYS, municipal and Central Register postings.
  3. Classify by trade and UNSPSC.
  4. Extract the deadline, pre-bid date, bond and insurance requirements and SBPP flag.
  5. Write a three-line plain-English summary and a go/no-go checklist.
  6. Send a digest plus deadline reminders, and track awards to show what won.
- **Human work:** pick the trade niche through about 15 customer interviews, and recruit association partners. Spot-check classifications weekly. Read the COMMBUYS, BidNet and municipal site terms before automating access. Handle support.
- **Caution:** COMMBUYS already sends free UNSPSC-based alerts, so the value has to come from municipal coverage, triage and plain language. The ProcureTap founder reported that trials did not convert under a paywall (see Q3).

#### 2. Local / niche small-nonprofit grant-deadline digest (Rank 2)
- **Data:** Grants.gov search2 API (federal), Massachusetts state grant pages (e.g., cultural council and agency NOFOs on mass.gov), community-foundation and family-foundation web pages (scraped), and corporate giving pages.
- **Group and benefit:** MA nonprofits with budgets under about $500K, or a national niche such as faith-based ministries, youth sports, arts collectives, food pantries or mutual-aid groups. They get deadlines and fit scores they currently assemble by hand.
- **Who pays:** the nonprofit at $15–$25/mo ($149–$199/yr), or B2B through a nonprofit association, community foundation or fiscal sponsor as a member benefit.
- **Path:** 35–50 subscribers at $19, or 2–3 association deals.
- **Agent workflow:**
  1. Crawl about 200–400 funder pages weekly.
  2. Extract eligibility, deadline, award size and geography.
  3. Match against each subscriber's profile (mission, budget, geography).
  4. Send a digest and calendar (.ics) feed.
  5. Draft an LOI skeleton per opportunity.
- **Human work:** build the funder seed list and verify a sample. Market through nonprofit networks.
- **Caution:** cheap incumbents exist. GrantStation costs $119–$199 via TechSoup and $139 via MA Council of Nonprofits membership, and GrantWatch costs $199–$249/yr (see Q2). The product must be clearly more local or more niche than these.

#### 3. Condition-specific clinical-trial alerts via patient organizations (Rank 3; best background fit)
- **Data:** ClinicalTrials.gov API v2, filtered by condition, recruiting status, location radius and last-update date.
- **Group and benefit:** a non-oncology community. Options that fit a psychology background include treatment-resistant depression, OCD, PTSD, ADHD, autism (caregivers) and Long COVID neuro symptoms. Others are rare-disease foundations without in-house trial navigators, or "Boston-area studies recruiting healthy volunteers / students." Members get alerts when a new site near them starts recruiting or eligibility changes, with plain-language criteria.
- **Who pays:** a patient-advocacy organization or rare-disease foundation pays a flat monthly sponsorship or white-label fee. Research sites could pay a flat, time-based listing fee, never a per-referral or per-enrollment fee (see Q4). Patients pay nothing.
- **Path:** 2–4 organizations at $200–$400/mo.
- **Agent workflow:**
  1. Run a nightly API delta.
  2. Parse eligibility criteria into a structured checklist.
  3. Generate a plain-language summary at about an 8th-grade reading level, with the NCT ID and the site contact.
  4. Send a geo-targeted digest.
  5. Optionally run a self-screen questionnaire that stores no data or stores it under HBNR-compliant practices.
- **Human work:** build organization partnerships, which is the hard part. Do clinical-accuracy review of summaries at first, ideally with a clinician advisor. Draft privacy policy and disclaimers.
- **Caution:** Antidote already gives a free embeddable matcher to about 250 organizations, funded by pharma. The differentiation is proactive alerts, condition depth and plain language.

#### 4. Massachusetts multi-city affordable-housing lottery and waitlist alerts (Rank 4; sponsor-only)
- **Data:** Boston Metrolist, Housing Navigator MA, Cambridge, Somerville and other municipal inclusionary pages, lottery-agent sites, and listings in local papers (lottery agents place listings in the Bay State Banner, for example [Flats at 8th](https://baystatebanner.com/real-estate-listing/flats-at-8th)).
- **Group and benefit:** low and moderate-income renters and first-time buyers, especially non-English speakers. The benefit is one SMS or email alert across municipalities, an AMI income pre-check, a deadline reminder and a document checklist.
- **Who pays:** it must be free to applicants. Charging people who are applying for affordable housing is exploitative and risks looking like an application-assistance scam. Possible payers are employers, hospitals or universities (as an employee benefit), credit unions (Harvard FCU already runs affordable-homeownership education), CDCs, or a small grant.
- **Path:** uncertain. One employer or credit-union sponsor at $500/mo would hit the target, but this is unproven.
- **Agent workflow:** poll sources daily, extract income limits, unit sizes and deadlines, run an eligibility pre-check from the user's self-reported household size and income, translate, and send alerts.
- **Human work:** win the sponsor, review fair-housing and affirmative-marketing compliance, and handle accuracy disputes.

#### 5. Building-permit lead alerts for micro-trades (Rank 5)
- **Data:** data.boston.gov Approved Building Permits, plus Cambridge and Somerville open data.
- **Group:** small subcontractors and suppliers, such as insulation, electricians, dumpster rental, or a Mass Save-eligible heat-pump installer. The benefit is earlier leads from permits in their trade and ZIP codes.
- **Who pays:** subscriptions of $39–$79/mo. Path: 10–20 contractors.
- **Agent workflow:** run a daily dataset diff, classify permit descriptions into work types, filter by trade and geography, add contractor-of-record context, and send a digest.
- **Human work:** sales to contractors and choosing a niche.
- **Caution:** Shovels and the Apify scrapers make the data layer cheap. The gap is only local curation, which makes this a thin moat.
- **Predatory flag:** selling code-violation, tax-delinquency or foreclosure lists to investors who target distressed homeowners exploits vulnerable owners. Exclude it.

#### 6. Drug-shortage / discontinuation alerts (Rank 6)
- **Data:** the openFDA drug shortages endpoint.
- **Group:** a condition community (e.g., ADHD-stimulant users), or small independent clinics and pharmacies.
- **Assessment:** the data is free and small (about 1,700 records), and many wrappers exist. Patient willingness to pay is likely low, and patient-facing advice risks crossing into medical advice. This works best as a free feature inside #3's sponsored product.

#### 7. Class-action settlement eligibility (Rank 7; avoid or free-plus-disclosed-ads)
- The market is saturated with apps and newsletters (see Q2), and fraud pressure on claims is high (see Q4). Weekly subscriptions for information that is free elsewhere are a predatory pattern.
- An ethical version would be a free niche digest, e.g., settlements relevant to students, renters or a particular product category, with no auto-filing. This is unlikely to reach $500/mo without law-firm advertising, which raises attorney-advertising issues (not researched).

#### 8. Massachusetts unclaimed property (Rank 8; avoid the finder model)
- The search is free at FindMassMoney, and finder agreements are legally constrained (see Q4).
- A benign variant is a B2B service that runs free lookups for a credit union's, nonprofit's or employer's members as a paid wellness perk, with no fee to the claimant. This is low priority.

#### 9. Narrow-demographic scholarships (Rank 9; do not charge students)
- Incumbents are free (Bold.org), and the FTC has long treated fee-charging scholarship search as a scam hallmark.
- The only ethical models are B2B (high-school counselors, community organizations) or sponsorship.

---

## Q2. For each candidate, what competitors exist, what they charge, and what gap remains?

### Takeaway
Procurement and grant intelligence have expensive enterprise tools (GovSpend at about $8.5K–$25K/yr, Instrumentl at $299+/mo, DrugPatentWatch at $1K+/mo) and cheaper mid-market tools (BidSync at $55+/mo, RFPSchoolWatch at $795/yr per state, GrantWatch at $199–$249/yr, GrantStation at $119–$699/yr). The gap is not price alone but locality, trade focus and plain-language triage. Clinical-trial matching, housing search and scholarships have strong free incumbents, so any paid layer must be sponsor-funded. Class-action apps are crowded with $4.99/week subscriptions.

### Cited Findings
**Government bids**
- Periscope BidSync's own pricing page: $55/mo (billed annually, one region), $105/mo (national state and local) and $234/mo (state, local, federal and military). The free Basic tier covers 400+ partner agencies, while Pro covers about 100K new bids per month. — [Periscope BidSync pricing](https://www.periscopeholdings.com/bidsync-pricing). This conflicts with Software Advice's listing of $59/$69/$119/mo. — [Software Advice](https://www.softwareadvice.com/construction/bidsync-profile)
- GovSpend does not publish pricing. Third-party estimates, from sites that sell competing products, put it at a median of about $11,576/yr (Vendr data, 31 purchases) and a range of $8,500–$24,750/yr. It reportedly requires a demo, offers no free trial, and is stronger on historical spend analytics than on live bid alerts. — [fed-spend.com 2026 comparison](https://fed-spend.com/blog/govwin-govspend-govtribe-bloomberg-pricing-compared-2026); [GovContractFinder pricing guide](https://govcontractfinder.com/tools/government-contracting-software-pricing-guide)
- BidNet Direct offers tiered paid plans with daily custom alerts, but no public price was found. — [Walturn guide](https://www.walturn.com/insights/bidnet-direct-and-beyond-navigating-public-procurement-platforms-for-startups); [Capterra](https://www.capterra.com/p/230530/BidNet-Direct/)
- RFPSchoolWatch (a K-12 niche) charges $795/yr for one state, with multi-state tiers above that. — [RFPSchoolWatch pricing](https://www.rfpschoolwatch.com/pricing)
- BidHits offers AI-broadened keyword alerts with a 14-day free trial. — [BidHits](https://www.bidhits.com/home.php)

**Grants**
- Instrumentl lists Discover at $299/mo annual or $349 monthly (3 users), Pre-Award at $499/$579 (5 users), Full Lifecycle at $999/$1,159 (15 users), and custom Enterprise pricing, all with a 14-day trial. — [aitoolsbakery](https://aitoolsbakery.com/blog/instrumentl-pricing/); [grantsights](https://grantsights.com/blog/instrumentl-pricing). A Visualping change log (Aug 2026) recorded Discover monthly changing from $349 to $326. — [Visualping](https://visualping.io/pages/instrumentl-pricing-alerts-4894411)
- GrantStation retails at $699/yr. It costs $199 via TechSoup, with a Fall 2026 promotion at $119 (Sept 15–16, 2026), and $139 for members of state nonprofit associations. — [TechSoup](https://support.techsoup.org/hc/en-us/articles/29273095360027-GrantStation-Savings-on-TechSoup); [TechSoup Fall 2026 promo](https://support.techsoup.org/hc/en-us/articles/29273015196699-Upcoming-Fall-2026-GrantStation-Promotion); [MA Council of Nonprofits](https://macouncilofnonprofits.org/?p=30045); [Maine Assoc. of Nonprofits](https://www.nonprofitmaine.org/products/grantstation-annual-subscription)
- GrantWatch shows two pricing sets depending on the regional page: $18/wk, $45/mo, $90/qtr and $199/yr, or "MemberPlus+" at $22/$49/$100/$249. — [Ohio GrantWatch](https://ohio.grantwatch.com/plans.php); [New Hampshire GrantWatch](https://newhampshire.grantwatch.com/plans.php)
- Candid / Foundation Directory pricing was not found (see Gaps).

**Clinical trials**
- Antidote Match is free for organizations to embed and was reported on about 250 organization websites, including the Lung Cancer Alliance, JDRF and Healthline. Pharma licenses its Match API and white-labels the tool. It raised $11M led by Merck GHI, for $26M total (2018–2020 coverage). — [FierceBiotech](https://www.fiercebiotech.com/cro/clinical-trial-matching-platform-raises-11m-backed-by-merck-s-tech-fund); [Pharmaphorum](https://pharmaphorum.com/news/merck-clinical-trial-matching-antidote); [PatientWorthy, 2018](https://patientworthy.com/2018/03/13/american-liver-foundation-antidote-launch-clinical-trial-matching-tool/)
- PlainTrial, a consumer trial site, states its trial data comes from ClinicalTrials.gov (public domain) while it owns its own presentation and editorial content. Plain-language trial products already exist. — [PlainTrial Terms](https://plaintrial.com/terms)
- An open-source MCP server wraps the ClinicalTrials.gov v2 API, including a "find eligible" patient-matching tool. — [GitHub: clinicaltrialsgov-mcp-server](https://github.com/cyanheads/clinicaltrialsgov-mcp-server)

**Housing**
- Housing Navigator Massachusetts is a free nonprofit search tool listing about 216,000 income-restricted units. It covers public housing, HUD-assisted, 40B, LIHTC, inclusionary and other housing, and advertises open waitlists and lotteries. — [SOAR coverage of disability commission testimony](https://cp.soar.com/articles/7016226/Massachusetts/Housing-Navigator-Massachusetts-tells-disability-commission-its-database-lists-216000-incomerestricted-units-and-is-free-to-use); [MHP](https://mhp.net/rental-financing/housing-navigator); [Boston 25 News](https://www.boston25news.com/news/-housing-navigator-tool-hopes-to-beone-stop-shopfor-affordable-housing-listings/1007497981)
- Boston Metrolist is free, with email notifications (see Q1).

**Building permits / violations**
- Shovels API v2 covers 130M+ permits and 2.3M+ contractor profiles across 1,800+ jurisdictions, with data refreshed on the 1st and 15th of each month. The free key is call-limited. — [Shovels API docs](https://shovels-v2.redoc.ly). Revenue comes from online/API subscriptions, usage credits and enterprise data licenses. — [Sacra](https://sacra.com/c/shovels/). One third-party directory shows about $599/mo (unverified). — [The GTM Directory](https://thegtmdirectory.com/tools/shovels)
- Apify permit actors charge about $30 per 1,000 results, or about $0.005 per permit and $0.01 per contractor enrichment. — [Apify building-permits-scraper](https://apify.com/4l3c/building-permits-scraper); [Apify building-permits-intel](https://apify.com/seibs.co/building-permits-intel)
- Tenant-side violation lookup is already served free: Boston's RentSmart tool and openigloo building pages. — [Next City](https://nextcity.org/daily/entry/boston-rentsmart-tool); [openigloo example](https://openigloo.com/building/boston/ecd7f0fb-0cfe-4bd7-93b7-84ceb8bbb70a/boston-roxbury-2-forest-pl-02119)

**Regulatory / pharma**
- DrugPatentWatch: Starter is $1,000/mo or $8,000/yr with no email alerts, Professional is $3,000/mo or $24,000/yr with custom alerts, and Enterprise is custom. — [DrugPatentWatch pricing](https://drugpatentwatch.com/pricing/)
- Multiple Apify actors wrap the openFDA shortages endpoint, including a "delta monitor" that flags new, resolved or updated shortages. — [Apify drug-shortage-delta-monitor](https://apify.com/malonestar/drug-shortage-delta-monitor)

**Class actions**
- Collect (Settlement Finder) charges $4.99/week up to $59.99/yr. — [App Store: Collect](https://apps.apple.com/app/id6752740187). Catch: Class Action Finder is "100% free". — [Catch listing](https://mwm.ai/apps/app/6752961879). ClaimHunt auto-bills premium plans. — [App Store: ClaimHunt](https://apps.apple.com/us/app/-/id6755202426). Open Class Actions has a free app ("coming soon") with editor-written listings from court documents. — [Open Class Actions](https://openclassactions.com/app)
- A Reddit user says they have subscribed to Top Class Actions "for years". Another recommends ClaimDepot's weekly newsletter as more complete. These are anecdotal. — [Reddit snapshot, Dec 2025](https://reddit.sentinel-team.org/posts/1pn8bpu/snapshots/2025-12-16T02%3A50%3A57.13602Z)

**Scholarships**
- Bold.org is free for students. Its pricing page says it earns revenue from partner companies when students use "vetted, optional resources". Over 70% of donors leave an optional tip, and it reports $16M disbursed to date. — [Bold.org donor pricing](https://bold.org/donors/pricing/); [Bold.org donor help](https://donorhelp.bold.org/en/articles/9941413-does-bold-org-charge-donation-fees); [Bold.org impact](https://bold.org/impact/)

### Inferences
- **Procurement:** a micro-business digest priced at $19–$49/mo would sit below BidSync's paid tiers and far below GovSpend. It must beat COMMBUYS' free alerts and BidSync's free tier on Massachusetts municipal coverage and plain-language triage, which is where the gap is.
- **Grants:** the price ladder is GrantStation at $119–$199 (discounted), GrantWatch at $199–$249/yr and Instrumentl at $3,588+/yr. A $15–$25/mo product competes mainly with GrantWatch and GrantStation, so it must win on locality (MA community foundations, municipal cultural councils) or vertical depth. The low end is moderately saturated.
- **Clinical trials:** Antidote's free embed model shows that patient groups expect matching for free and that the money comes from pharma or sites. A solo operator can realistically charge organizations for curated alerts and content, not for basic search.
- **Building permits:** the data layer is saturated (Shovels plus Apify), and only hyper-local trade curation remains.
- **Class actions and scholarships:** saturated with free options, and the existing paid apps lean on weekly subscriptions. These are not good targets.

### Gaps
- BidNet Direct and Candid (Foundation Directory) pricing were not found.
- Shovels' official price is unverified.
- Current pricing for Top Class Actions or ClaimDepot (likely ad-supported) was not found.
- Whether Housing Navigator MA offers email or SMS alerts is unconfirmed.
- No MA-specific municipal-bid aggregator was identified. This could mean a gap or a search miss; check before building.

---

## Q3. Who has demonstrated willingness to pay?

### Takeaway
Willingness to pay is clearly demonstrated by businesses and nonprofits buying bid and grant intelligence at $55–$1,000+/mo. Solo founders who build on free government data report small, slow traction, roughly $99–$1,300 MRR. Individuals in need (housing applicants, patients, students) show little willingness to pay, and charging them is often a red flag. The $500–$1,000/mo target is plausible for B2B niche digests but needs real distribution work; build quality alone will not get there.

### Cited Findings
- ProcureTap, a solo product aggregating about 70K live US bids from 605 agencies refreshed every 6 hours, self-reported $99 MRR (1 paying customer, 1 in trial) on about $40/mo infrastructure. The founder reported 0 of 7 trial signups converting while a paywall was in place, and SEO driving growth (self-reported, unverified). — [Indie Hackers: ProcureTap](https://www.indiehackers.com/product/procuretap)
- Grants For Creators, a grants newsletter by Danielle Desir-Corbett, reportedly reached about $1,300/mo in recurring revenue. Its price was not given. — [Side Hustle Nation](https://www.sidehustlenation.com/paid-newsletters/)
- A niche Substack, Faith Based Grants Newsletter, serves ministries, churches and Christian nonprofits, which suggests vertical grant digests exist. Its price was not visible. — [Faith Based Grants Newsletter](https://faithbasedgrants.substack.com)
- A developer article titled "The $459/mo grant alert industry runs on a free government API" exists. Its content could not be retrieved, so only the title is evidence. — [dev.to](https://dev.to/scrapemint/the-459mo-grant-alert-industry-runs-on-a-free-government-api-1kdp)
- Paying buyers: GovSpend's median contract of about $11.6K/yr across 31 verified purchases (third-party Vendr data) shows organizations pay for procurement intelligence. — [fed-spend.com](https://fed-spend.com/blog/govwin-govspend-govtribe-bloomberg-pricing-compared-2026)
- Nonprofit associations bundle GrantStation as a paid member benefit ($139 for members versus $699 retail), so associations act as channels for grant tools. — [MA Council of Nonprofits](https://macouncilofnonprofits.org/?p=30045); [Maine Assoc. of Nonprofits](https://www.nonprofitmaine.org/products/grantstation-annual-subscription)
- Pharma and sites pay for trial matching rather than patients: Antidote licenses its API to pharma and was funded by Merck GHI. — [Pharmaphorum](https://pharmaphorum.com/news/merck-clinical-trial-matching-antidote)
- Research units pay participant referral stipends: up to $1,000 per referral (Altasciences) and $50 per qualified referral (Revival Research). This shows sites value recruitment, though see Q4 on ethics. — [Altasciences](https://participantsla.altasciences.com/node/154); [Revival Research](https://revivalresearch.org/?p=16830)
- In one trial, recruitment cost about £132 per referral and £377 per randomized participant. — [Trials journal](https://trialsjournal.biomedcentral.com/articles/10.1186/s13063-021-05348-9/tables/5)
- Consumers do pay for settlement-finder apps: Collect's $4.99/wk to $59.99/yr tiers exist. No subscriber counts were found. — [App Store: Collect](https://apps.apple.com/app/id6752740187)
- Credit unions run affordable-homeownership education that covers lotteries (Harvard FCU, Feb 2026), which makes them a possible sponsor for housing alerts. — [Harvard FCU](https://harvardfcu.org/wp-content/uploads/2026/02/Harvard-FCU_HBFday3_Affordable.pdf)

### Inferences
- ProcureTap's data point (a broad national feed, no conversions behind a paywall) suggests broad aggregation does not sell. A narrow trade-and-state niche with a free weekly digest plus a paid daily/alerts tier is the more plausible funnel.
- The most reliable route to $500–$1,000/mo for a student operator is one or two B2B or association deals rather than 30+ individual subscribers, because associations already buy tools for members (GrantStation precedent).
- For trial alerts, the payer is the organization (an advocacy group or site), mirroring Antidote. A $200–$400/mo flat fee is my estimate, not an observed price.

### Gaps
- No subscriber counts were found for any paid bid-alert or grant newsletter beyond ProcureTap and Grants For Creators.
- No forum evidence was collected specifically from Massachusetts micro-contractors complaining about COMMBUYS or municipal bid discovery. Customer interviews are needed.
- No evidence was found of advocacy organizations paying flat fees for third-party trial alerts. This is an assumption to test.

---

## Q4. Legal constraints (data licensing, MA unclaimed-property finder rules, FCRA, HIPAA/health privacy, accuracy/liability, CAN-SPAM/TCPA)

### Takeaway
Most of the source data is public US government data. The main legal risks come from how the product is monetized and what it collects, not from the data itself:
- per-referral fees in clinical trials are considered unethical;
- Massachusetts finder agreements are restricted (reportedly void within 24 months and capped at 10%, though the primary text could not be verified);
- health apps outside HIPAA fall under the FTC Health Breach Notification Rule;
- fee-based scholarship search is a long-standing FTC scam pattern;
- SMS alerts need TCPA consent, though the stricter FCC one-to-one rule was vacated in January 2025.

### Cited Findings
**Unclaimed property (Massachusetts)**
- Massachusetts holds about $3.4B in unclaimed property, and roughly 1 in 10 residents is owed money. The Treasurer's Feb 2026 release cited 118,000 claims processed and $237M returned last year. AP coverage cited $125M returned, a conflict between sources. The $3.4B figure also appears in 2021 releases, so it may be a repeated figure rather than a new count. — [MA Treasury release, Feb 2026](https://www.masstreasury.org/single-post/treasurer-goldberg-announces-latest-release-of-unclaimed-property-listings); [Reading Post, Feb 2026](https://thereadingpost.com/2026/02/27/treasurer-goldberg-announces-latest-release-of-unclaimed-property-listings-2/); [WHDH/AP](https://whdh.com/news/state-lists-forgotten-bank-accounts-other-unclaimed-items/)
- Claiming is free, there is no time limit, and claimants often receive interest. — [Reading Post](https://thereadingpost.com/2026/02/27/treasurer-goldberg-announces-latest-release-of-unclaimed-property-listings-2/)
- A third-party summary says MA caps finder fees at 10% (citing c. 200A § 9A), says contracts signed within 24 months of the state receiving property are unenforceable, and says the Treasury warns that upfront "processing fees" are likely fraudulent. The statute text could not be verified because malegislature.gov was unreachable. — [ungovr.org MA](https://www.ungovr.org/unclaimed/ma)
- A Rhode Island Treasurer's 2024 legislative testimony describes Massachusetts as having a two-year bar on finder agreements, citing 960 CMR 4.06. — [RI Legislature, H7569 testimony, Mar 2024](https://rilegislature.gov/Special/comdoc/House%20Judiciary%202024/03-05-2024--H7569--The%20Honorable%20James%20A.%20Diossa,%20RI%20General%20Treasurer.pdf)
- Conflicting signal: a 2019 MA bill that would have voided agreements made within 24 months of payment to the Treasurer and capped fees at 10% died at the end of the 2019–2020 session. Similar 2017 bill text (H35) proposed a 10% cap and a $100 annual locator registration. — [BillTrack50](https://www.billtrack50.com/billdetail/1079404); [MA H35 (2017)](https://malegislature.gov/Bills/190/H35.pdf); [MA H54 (2019)](https://malegislature.gov/Bills/191/H54.Html)
- Comparable statutes: Maine voids locator agreements made within 24 months and caps fees at 15% for months 24–36. Illinois caps fees at 10%. — [Maine 33 MRS § 2201](https://legislature.maine.gov/statutes/33/title33sec2201.html); [765 ILCS 1026/15-1302](https://lig.ilga.gov/legislation/ilcs/documents/076510260K15-1302.htm)
- Enforcement example: Indiana's Attorney General obtained $107,000 from a California finder company over allegedly misleading solicitations about unclaimed property. — [The Reporter](https://readthereporter.com/?p=164027)

**Clinical trials / health data**
- WCG's guidance says per-referred-patient fees are "not considered to be appropriate". Compensation should be for time and effort (hourly, or per record reviewed) and should not depend on eligibility or enrollment. The AMA Code of Medical Ethics prohibits finder's fees for trial referrals. — [WCG Clinical, Ch. 42](https://www.wcgclinical.com/?p=27719)
- The FTC's amended Health Breach Notification Rule (final April 26, 2024; effective July 29, 2024) explicitly covers health apps and online services not subject to HIPAA. It defines breach to include unauthorized voluntary disclosures, not just hacks, and requires notice to individuals, the FTC and sometimes the media. — [Nixon Peabody, May 2024](https://www.nixonpeabody.com/insights/alerts/2024/05/22/ftc-amends-and-broadens-health-breach-notification-rule); [McDermott](https://www.mwe.com/?p=279089)
- ClinicalTrials.gov's archived (2004) terms say its data is available to all requesters at no charge and that the terms apply regardless of how the data was obtained. Current terms could not be retrieved. — [Archived CT.gov terms, 2004](https://webharvest.gov/peth04/20041014214437/http://clinicaltrials.gov/ct/info/termsandcs)

**Class actions**
- Claim fraud has exploded. One industry source reports more than 80M claims with "significant indicia of fraud" in 2023, versus about 400K in 2021. In the Godiva settlement, 47% of 825K+ claims were invalidated after a bot was discovered. Third-party filers (TPFs) solicit class members to file on their behalf, and bot volume can jeopardize court approval of settlements. — [Class Defense Blog, Aug 2024](https://www.classdefenseblog.com/2024/08/the-implications-of-skyrocketing-fraudulent-claims-in-class-action-settlements/); [Ontario Bar Assoc.](https://oba.org/attack-of-the-bots-how-fraud-threatens-the-integrity-of-class-action-settlements/); [BrownGreer](https://www.browngreer.com/news/blog-attack-of-the-bot-filings/); [Angeion: third-party filers](https://www.angeiongroup.com/news/pros-and-cons-of-third-party-filers)

**Scholarships**
- FTC (1996–97 "Project $cholar$cam"): no legitimate search service guarantees a scholarship. Scammers charged $10–$400 upfront, often with near-impossible refund conditions. This is older but still widely repeated guidance. — [FTC press release, Nov 1997](https://www.ftc.gov/news-events/news/press-releases/1997/11/ftc-continues-crackdown-scholarship-search-service-con-artists)

**SMS alerts (TCPA)**
- On January 24, 2025, the Eleventh Circuit (*Insurance Marketing Coalition v. FCC*) vacated the FCC's one-to-one consent rule. Prior express written consent requirements still apply for marketing texts. — [Kelley Drye](https://www.kelleydrye.com/viewpoints/blogs/ad-law-access/eleventh-circuit-vacates-tcpa-11-consent-rule); [K&L Gates, Feb 2025](https://www.klgates.com/thought-leadership/Loper-Bright-Strikes-Again-Eleventh-Circuit-Hangs-Up-on-FCCs-One-to-One-Consent-Rule-Calling-the-Validity-of-Other-TCPA-Rules-Into-Question-2-3-2025)

### Inferences
- **Unclaimed property:** do not build a finder business that charges claimants. The search is free, the fee window is restricted, and the model targets people who just don't know about a free process. If pursued at all, use only a B2B, no-fee-to-claimant model.
- **Trial alerts:** charge organizations a flat subscription. Never tie payment to referrals, eligibility or enrollment. Avoid collecting identifiable health information if possible. Send alerts by condition and ZIP chosen by the user, and if self-screen answers are stored, treat the product as HBNR-covered: write a privacy policy, sell no data, and have a breach plan.
- **Data licensing:** federal data (CT.gov, Grants.gov, SAM.gov, openFDA) is generally public domain. Municipal portals (data.boston.gov) publish open datasets. COMMBUYS, BidNet and Central Register content may carry terms of use or subscription restrictions, so the human must review them before scraping. The Central Register is a paid subscription, so redistributing its full text may be restricted.
- **Accuracy and liability:** every alert should link to the official source, state "verify with the issuing agency", and avoid eligibility guarantees. This matters especially for housing (income limits) and trials (eligibility).
- **FCRA:** an alert about opportunities sent to the person who subscribed is unlikely to be a "consumer report". Selling lists of identified individuals (code-violation owners, unclaimed-property owners) to third parties is the riskier pattern. This is my unverified reasoning; see Gaps.

### Gaps
- CAN-SPAM requirements and current penalty amounts, and FCRA/CFPB data-broker developments, could not be researched because the web-search budget was exhausted. Check the FTC CAN-SPAM compliance guide and the current CFPB position on data brokers.
- The current official MA c. 200A § 13 / 960 CMR 4.06 text was not verified, because malegislature.gov was unreachable. The 10% cap and 24-month bar rest on secondary sources plus RI testimony.
- IRB and FDA rules on trial recruitment advertising (whether condition-alert content needs IRB-approved language) were not researched.
- Fair-housing advertising and affirmative-marketing rules for third-party lottery alert services were not researched.
- Attorney-advertising rules (MA Rule 7.2) for class-action lead-generation models were not researched.

---

## Q5. Which official APIs or bulk-data feeds exist?

### Takeaway
- **Free, keyless or near-keyless APIs** exist for ClinicalTrials.gov v2, Grants.gov (search2 / fetchOpportunity) and openFDA drug shortages.
- **SAM.gov** needs an API key with a tight daily quota for non-federal users.
- **data.boston.gov** publishes building permits and violations datasets.
- **Massachusetts procurement data** (COMMBUYS, Central Register, municipal sites) has no confirmed public API, so it likely needs careful scraping or manual workflows. That is both the moat and the legal risk.

Official documentation pages for SAM.gov, ClinicalTrials.gov and openFDA could not be fetched from this environment, so these details are second-hand.

### Cited Findings
- **Grants.gov:** launched RESTful search2 and fetchOpportunity APIs that require no authentication (April 2025 report). — [Univ. of Florida College of Education, Apr 2025](https://education.ufl.edu/educational-research/2025/04/04/grants-gov-introduces-new-restful-apis-to-streamline-grant-search-and-retrieval/); [Simpler.Grants.gov API wiki](https://wiki.simpler.grants.gov/product/api). Third-party scrapers handle HTTP 429, so rate limiting is possible. — [Apify Grants.gov scraper](https://apify.com/publicrecords/grants-gov-scraper)
- **SAM.gov Get Opportunities API:** requires an API key. Third-party sources report about 10 calls/day for non-federal accounts without a SAM role and 1,000/day with one. Another source says 40/day for new non-federal accounts. Keys reportedly expire every 90 days. These figures conflict and are unverified. — [Cleat.ai SAM.gov API guide](https://www.cleat.ai/developers/sam-gov-api); [Apify foxlabs/sam-gov](https://apify.com/foxlabs/sam-gov)
- **ClinicalTrials.gov API v2:** public, with no key or account per community tools. A community listing gives about 50 requests/minute (unverified). An open-source MCP server rate-limits itself to about 1 request/second. — [skillselion listing](https://skillselion.com/skills/jimmc414/kosmos/clinicaltrials-database); [Apify CT.gov search](https://apify.com/kdhan/clinicaltrials-gov-search); [GitHub MCP server](https://github.com/cyanheads/clinicaltrialsgov-mcp-server)
- **openFDA drug shortages:** served at `api.fda.gov/drug/shortages.json`. It is keyless JSON of about 1,700 records, paged at 1,000 per request, with current, resolved, to-be-discontinued and discontinued statuses. — [Apify compute-edge](https://apify.com/compute-edge/fda-drug-shortages-scraper); [Apify automation-lab](https://apify.com/automation-lab/fda-drug-shortages-scraper)
- **data.boston.gov:**
  - Approved Building Permits is published by DoIT with ISD as contact. It excludes in-process, denied, void and revoked permits. The start year is listed as 2009 on the portal versus 2015 elsewhere, and the last-modified date seen was April 2024. — [Approved Building Permits](https://data.boston.gov:443/dataset/approved-building-permits); [Boston GIS item info](https://gis.boston.gov/arcgis/rest/services/ISD/approved_building_permits/MapServer/info/iteminfo)
  - Public Works Violations is updated daily from December 2012. Building and Property Violations (ISD) has an unconfirmed update frequency. — [Public Works Violations](https://data.boston.gov/dataset/public-works-violations); [Building and Property Violations](https://data.boston.gov/dataset/building-and-property-violations1)
- **COMMBUYS:** postings are public, and free Seller registration enables notifications. No public API was found. — [Mass.gov required specs](https://www.mass.gov/doc/g-required-specs/download)
- **Central Register / Goods and Services Bulletin:** available by subscription from the Secretary of State's office. — [New Bedford FAQ](https://www.newbedford-ma.gov/purchasing/?p=20)
- **Unclaimed property:** searchable free at FindMassMoney. The domain appears as both .com and .gov across sources, and no bulk feed was identified. — [MA Treasury release](https://www.masstreasury.org/single-post/treasurer-goldberg-announces-latest-release-of-unclaimed-property-listings); [WHDH/AP](https://whdh.com/news/state-lists-forgotten-bank-accounts-other-unclaimed-items/)
- **Shovels** offers a free-tier API key (call-limited) as a commercial alternative for multi-jurisdiction permits. — [Shovels API docs](https://shovels-v2.redoc.ly)

### Inferences
- Agent stack cost is low. ProcureTap reported about $40/mo infrastructure, and most feeds are free, so the main costs are LLM tokens for summarization and an email/SMS provider. This fits a low-capital student.
- SAM.gov's tiny non-federal quota (if about 10/day is accurate) means a MA-federal-set-aside feed should use a few broad daily queries with caching, or the bulk extracts (not verified here).
- The Massachusetts municipal-bid niche (#1) lacks an API, which keeps competitors out but makes the agent's scraping layer fragile. The human must monitor for breakage and terms-of-use issues.

### Gaps
- Official rate limits, terms and attribution requirements for SAM.gov, ClinicalTrials.gov and openFDA were not verified, because their documentation sites were unreachable (DNS errors).
- Whether Mass.gov or COMMBUYS offers any open-data export of bids was not confirmed.
- Whether data.boston.gov's permits dataset is still refreshed daily in 2026 was not confirmed; the last-modified date seen was 2024.
- No confirmed data source for Cambridge permits or lotteries was retrieved; searches returned only Somerville material.
- Applicants-per-unit figures for Boston lotteries, a key demand metric, were not found.
- IRS Form 990 bulk data (for building grant-funder lists) and the ASHP drug-shortage database were not researched.
