# At-Home Neuroscience Projects and Small Experiments for a BU Student (as of October 2026)

Scope note: Researched 2026-10-14. Profile: a BU student aged 21 or older in Massachusetts, with a psychology research and statistics background and a low budget. WebFetch failed with DNS errors for some sites, such as boslab.org, so most findings come from search-result snippets of primary pages (manufacturer stores, government and legislature sites, university policy pages). Prices conflict across vendor pages in many places. Both figures are given where that happens. Anything dated before 2025 is marked [OLDER].

---

## 1. Consumer and open-source neurotech: prices, data access, and which experiments each device supports

### Takeaway
On a low budget, the best value is a Muse 2 (~$250) with the Mind Monitor app (~$15–18) for raw-data EEG. Published validation exists for Muse alpha/spectral measures and ERPs (N200/P300). For EMG/ECG/EOG and a basic P300 demo, a Backyard Brains Human SpikerBox (~$300) or a BITalino kit (~€190) also works. OpenBCI (Ganglion ~$625, Cyton ~$1,249) is the open-hardware research-grade step up. Emotiv headsets need a paid EmotivPRO subscription to export data. Neurosity and Galea are poor value for this budget.

### Cited Findings

**OpenBCI**
- Cyton (8-channel) board is listed at $1,249.00 on several OpenBCI shop pages (e.g., the EMG collection) and at $999.00 on another. Ganglion (4-channel) is listed at $624.99 and at $499.00. The higher prices appear on more listings and are probably current. — [OpenBCI shop, bioamplifiers](https://shop.openbci.com/collections/bioamplifiers); [OpenBCI shop, EMG](https://shop.openbci.com/collections/openbci-products/EMG)
- [OLDER] The Ganglion's original Kickstarter price was about $99–$100. That is historical, not current. — [Wikipedia: OpenBCI](https://en.wikipedia.org/wiki/OpenBCI); [Techdirt](https://www.techdirt.com/tag/open-hardware/)
- Galea (EEG/EMG/EOG/EDA/PPG built into a VR headset) is an enterprise device. Prices conflict: $25,000 (Varjo Aero) or $34,000 (Varjo XR-3) on OpenBCI's Galea Beta page, versus $42,980 on the US shop page. — [OpenBCI Galea page](https://shop.openbci.com/zh-cn/products/galea); [Freethink](https://www.freethink.com/ar-vr/galea-beta); [OpenBCI shop](https://shop.openbci.com/collections/frontpage/openbci)
- Galea's software suite exposes sensor data in Unity, Python, and "all BrainFlow-supported languages." Raw data is available through open-source protocols like BrainFlow. — [OpenBCI Galea page](https://shop.openbci.com/zh-cn/products/galea); [Skarredghost 2021](https://skarredghost.com/2021/02/12/openbci-galea-valve-index-bci/)

**Muse (Interaxon)**
- Muse 2 headband: $249.99 USD on choosemuse.com (also $249.99 at the Mayo Clinic store). The guided bundle is $309.00. The launch price was $249. — [Choose Muse: Muse 2](https://choosemuse.com/muse-2/); [Mayo Clinic store](https://store.mayoclinic.com/muse-2-headband.html); [TechRadar review](https://www.techradar.com/reviews/muse-2-review)
- Muse S Athena (launched March 2025): $474.99 USD. It adds fNIRS-style brain blood-oxygen measurement to EEG. — [Choose Muse: Athena](https://choosemuse.com/products/muse-s-athena); [BusinessWire press release](https://secure.businesswire.com/news/home/20250318250704/en/Introducing-Muse-S-Athena-The-Next-Evolution-in-Cognitive-Fitness)
- Raw data access: the third-party Mind Monitor app records raw microvolt EEG, absolute band powers, and accelerometer/gyro to CSV. It can also stream over OSC/Wi-Fi to a PC. App Store price is $14.99 or $17.99 (varies by listing). An EEGLAB plugin (`import_muse`) reads Mind Monitor CSVs for Muse 1, 2, and S. — [Mind Monitor App Store](https://apps.apple.com/us/app/id988527143); [musemonitor.com](https://musemonitor.com/); [import_muse GitHub](https://github.com/amisepa/import_muse)
- Some university labs use the "Muse Data Portal" to store and download raw EEG. — [University of Antwerp Social Lab](https://www.uantwerpen.be/en/research-facilities/antwerp-social-lab/research-tools/muse/)
- Validation, ERPs [OLDER, 2017]: Krigolson et al. showed the Muse captures the N200 and P300 in a visual oddball task and the reward positivity in a reward-learning task. ERP research worked with a Muse plus a single computer, without hardware event markers. Open-source code was released. These are the authors' own results. — [Krigolson et al. 2017, Frontiers in Neuroscience (PMC)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5344886/)
- Validation, spectral [OLDER, 2021]: Cannard, Wahbeh & Delorme compared Muse to a 64-channel BioSemi system. They report Muse is usable for power spectral density, individual alpha frequency, and frontal alpha asymmetry. — [bioRxiv preprint](https://www.biorxiv.org/content/10.1101/2021.11.02.466989.full.pdf); [Noetic summary](https://noetic.org/publication/validating-the-wearable-muse-headset-for-eeg-spectral-analysis-and-frontal-alpha-asymmetry/)
- Validation, language ERPs: an MTSU thesis found N1, P2, and N400 with the Muse 2. Condition differences were significant in one task but not the other. — [MTSU JewlScholar](https://jewlscholar.mtsu.edu/handle/mtsu/7187)
- Validation, sleep: a SLEEP conference abstract (not a full paper) reports Muse-S automated sleep staging agreed with polysomnography at 88–96% accuracy across stages. — [SLEEP abstract, DOI 10.1093/sleep/zsae067.01119](https://www.citedrive.com/en/discovery/1119-validation-of-a-portable-sleep-electroencephalography-device-in-good-sleepers-and-people-with-sleep-apnea/)

**Emotiv**
- Headsets: MN8 (2-channel EEG earbuds) $399; Insight (5-channel) $499; EPOC X (14-channel) $999 on the shop and blog, but $1,199 on Emotiv's comparison page. — [Emotiv headset price guide](https://www.emotiv.com/blog/emotiv-headset-price-guide); [Emotiv comparison](https://emotiv.com/comparison)
- Data access is paywalled. The free PRO-Lite tier lets you view raw EEG but not export it, and caps you at 5 recordings. Emotiv itself says PRO-Lite "is insufficient for research purposes." EmotivPRO Standard is $89/month or $1,068/year and adds record/store/export. Standard Team is $2,689/year. — [Emotiv PRO-Lite KB](https://www.emotiv.com/knowledge-base/pro-lite-capabilities); [EmotivPRO licensing table](https://www.emotiv.com/pages/pro-licensing-table-v1)
- Emotiv says its products are for "research applications and personal use only." Separate Student/Academic tiers exist. — [Emotiv PRO license updates](https://www.emotiv.com/blog/pro-license-updates-new-features-and-licensing-options)

**Neurosity Crown**
- Prices conflict: $1,199 (Outliyr product page and a 2026 roundup), $1,499 (another version of that roundup), and $899 (undated Self Research listing). It is developer-oriented, with JavaScript and Python SDKs. — [Outliyr: Neurosity Crown](https://outliyr.com/shop/neurosity-crown); [Outliyr neurofeedback roundup](https://outliyr.com/best-home-neurofeedback-devices); [Self Research library](https://library.selfresearch.org/devices/the-crown-neurosity/)

**Backyard Brains**
- Human SpikerBox: $299.99 direct. It records EMG, EKG, EEG, and EOG. The kit includes an EEG headband, gel, and sticker electrodes. The documentation includes a P300 EEG experiment, EMG setups, and autonomic stress (cold-pressor) experiments. The free Spike Recorder software does real-time display and data export. Ward's resells it for $365.70. — [Backyard Brains Human SpikerBox](https://backyardbrains.com/products/human-spikerbox); [Human SpikerBox docs](https://docs.backyardbrains.com/human/human-spikerbox); [Ward's](https://www.wardsci.com/us/en/product/NA5263252/human-spikerbox-new)
- Neuron SpikerBox Classic, for invertebrate extracellular recording such as a cockroach leg: $149.99 or $189.99 on Backyard Brains' own pages. Ward's institutional prices are $252.50–$263.90 for the Classic and $297.95–$311.40 for the Pro. — [Backyard Brains shop](https://shop.backyardbrains.com/products/neuron-spikerbox); [Backyard Brains Classic](https://backyardbrains.com/products/neuron-spikerbox-classic); [Ward's](https://www.wardsci.com/us/en/product/NA4630778/backyard-brains-neuron-spikerbox)
- RoboRoach ethics [OLDER, 2013 coverage]: PETA filed complaints with Michigan authorities, arguing that implanting the kit amounts to unlicensed veterinary practice. Backyard Brains said it breaks no laws. It anesthetizes roaches with ice water on the assumption that they may feel pain. It has acknowledged the experiments are "not philosophically perfect" and controversial, but says the benefits outweigh the costs. A Live Science op-ed called it "bad citizen science." No outcome of the PETA complaint was found. — [Slate 2013](https://www.slate.com/blogs/future_tense/2013/11/05/backyard_brains_roboroach_peta_protests_idea_of_cyborg_cockroaches.html); [Crowdfund Insider](https://www.crowdfundinsider.com/2013/11/25704-peta-files-complaint-kickstarter-grad-roboroach/); [Live Science op-ed](https://www.livescience.com/40821-roboroach-is-inhumane.html); [The Scientist](https://www.the-scientist.com/controlling-cockroaches-38578)

**BITalino (PLUX)**
- BITalino (r)evolution Board Kit BLE/BT: €189. It has EMG, ECG, EDA, EEG, accelerometer, and light sensors, plus a pushbutton. The "BITalino Board" kit is listed at €195 (sale) and BITalino Plugged (modular sensors) at €225. [OLDER] Earlier coverage cited €149. — [PLUX Board Kit](https://www.pluxbiosignals.com/products/bitalino-revolution-board-kit-ble-bt); [PLUX BITalino Board](https://www.pluxbiosignals.com/products/bitalino-board); [PLUX Plugged](https://www.pluxbiosignals.com/products/bitalino-plugged)

**Brain stimulation (do not do at home)**
- [OLDER, 2017] Most consumer tDCS devices make no medical claims, so the FDA never reviews them. Experts cite risks from amateur administration and unknown long-term effects. A commentary lists skin burns, seizures, mood swings, memory impairment, and worsening depression as possible adverse effects. — [NPR 2017](https://www.npr.org/sections/alltechconsidered/2017/01/07/507133313/students-zap-their-brains-for-a-boost-for-better-or-worse); [KQED](https://www.kqed.org/futureofyou/321859/theres-a-diy-brain-stimulation-community-despite-warnings)

### Inferences
- Rough fit of budget to experiment:
  - **Under $300:** Muse 2 + Mind Monitor. Supports eyes-open/closed alpha, individual alpha frequency, frontal alpha asymmetry, meditation-state spectral comparisons, and oddball P300/N200 (following Krigolson's open code). It is weak for anything needing central or parietal coverage beyond its four electrodes, or for precise event timing.
  - **About $300:** Human SpikerBox or BITalino. Good for EMG (fatigue, motor-unit recruitment, reaction time), ECG/HRV under stress (cold pressor), EOG blinks, and a basic single-channel P300. The SpikerBox is better documented for teaching. BITalino gives more modalities, including EDA.
  - **About $625–$1,250:** OpenBCI Ganglion or Cyton. This is the open hardware most often used in student BCI projects and hackathons. Use it for motor-imagery, multichannel ERP, and (likely) SSVEP projects.
- A statistics-strong student can add value by doing what consumer-EEG validation papers rarely do: reliability or replication analyses. Examples are test-retest of individual alpha frequency or frontal alpha asymmetry across days, Bayesian estimation of P300 effect sizes from a few sessions, or comparing artifact-rejection pipelines on Muse data. Krigolson 2017 and Cannard 2021 are templates.
- Emotiv's $1,068/year export license wipes out its hardware price advantage for this user. Prefer Muse, OpenBCI, BITalino, or Backyard Brains, which export data at no ongoing cost.
- Vendor apps (Muse, Emotiv, Neurosity) may upload neural data to company servers. Read the privacy policy before recording other people, and see Section 4.

### Gaps
- No source confirmed SSVEP performance on Muse, Ganglion, or Cyton, or OpenBCI-specific validation studies. A targeted search of OpenBCI docs or BrainFlow would be needed.
- Current Muse S (Gen 2) price and the current Mind Monitor CSV spec (sampling rate, units) were not confirmed.
- Cyton and Ganglion prices conflict between OpenBCI shop pages ($1,249 vs $999; $624.99 vs $499). Neurosity Crown also conflicts ($899 / $1,199 / $1,499).
- The Reddit communities r/OpenBCI, r/BCI, and r/neuroscience were not reachable or searched in a way that produced citable content.
- No independent replication of the Krigolson Muse ERP validation was found.
- A search result pointed to a conference paper comparing g.tec and Emotiv for P300 detection (possibly [Maynooth eprint](https://mu.eprints-hosting.org/id/eprint/15551/1/CM_validation.pdf)), but I could not verify its content. Peer-reviewed validation of Emotiv for ERPs is therefore unconfirmed here.

---

## 2. Online behavioral experiments: PsychoPy/Pavlovia, jsPsych, Gorilla, and Prolific — costs and solo feasibility

### Takeaway
A solo student can build experiments for free in jsPsych (hosted free on Cognition.run or self-hosted JATOS) or PsychoPy. Gorilla is free to build and pay-per-participant. Pavlovia is cheap per session, but its institutional licenses run £2,000+/year, so check whether BU already has one. Participant pay on Prolific is the real cost: at least $8/hr (recommended $12/hr) plus a 33.3% academic fee. A 100-person, 15-minute study at the recommended rate costs about $400. Any study meant for publication needs IRB review first (Section 4).

### Cited Findings
- **Prolific pay floor:** absolute minimum £6.00 / $8.00 per hour, recommended £9.00 / $12.00 per hour. Bonuses don't count toward the minimum. — [Prolific help: participant rewards](https://researcher-help.prolific.com/en/article/9cd998)
- **Prolific platform fee:** 42.8% on top of participant pay for corporate accounts, and 33.3% for academia and non-profits. The academic rate requires an institutional email and choosing the Academia account type. Participants receive the full reward. — [Prolific help: pricing](https://researcher-help.prolific.com/en/articles/445239-what-is-your-pricing)
- [OLDER / conflicting] A Prolific marketing page still lists a 30% industry and 25% academic fee. It appears outdated next to the help center. — [Prolific vs MTurk page](https://www.prolific.com/prolific-vs-mturk)
- **Prolific–Pavlovia integration** is documented by Prolific. — [Prolific: Pavlovia integration guide](https://researcher-help.prolific.com/en/articles/445190-pavlovia-integration-guide)
- **Pavlovia:** works with either an institutional license or per-participant credits. Official psychopy.org pricing tiers are £2,000–£5,200/year, all with unlimited accounts and experiments for the institution. [OLDER] A forum post cites a licence of £1,800 + VAT/year or credits at 24p + VAT per session. A PsychoPy comparison page cites £0.26 per participant. — [PsychoPy pricing](https://psychopy.org/pricing.html); [PsychoPy vs Gorilla](https://psychopy.org/about/comparing_PsychoPy_and_Gorilla.html); [PsychoPy discourse](https://discourse.psychopy.org/t/thanks-wellcome-trust-for-2-very-productive-years/10430)
- Some universities hold Pavlovia site licenses that give users automatic unlimited data collection, for example Yale (@yale.edu) and, through Oct 2025, the University of Michigan Psychology Department. — [Yale BrainWorks](https://research.yale.edu/cores/brainworks/pavlovia); [UMich LSA](https://teamdynamix.umich.edu/TDClient/47/LSAPortal/KB/Article/6572/Pavlovia-Department-of-Psychology-site-license)
- **Gorilla:** sign-up and building tasks, questionnaires, and experiments are free. You pay per participant, one token per participant per experiment. Per-participant prices conflict: £1.09 (PsychoPy comparison page), £0.75 (older Gorilla page), and £1.50/token public-sector rate (Gorilla FAQ). Academic discounts exist. — [Gorilla pricing FAQ](https://support.gorilla.sc/support/pricing-faq); [PsychoPy vs Gorilla](https://psychopy.org/about/comparing_PsychoPy_and_Gorilla.html)
- **jsPsych hosting:** Cognition.run is free and built for jsPsych. [OLDER, 2021] A Sussex guide warns it is run by one person and may not stay free. JATOS is free software you run on your own server. — [Sussex online experiments: hosting](https://users.sussex.ac.uk/mel29/online_experiments/hosting.html); [Sussex blog 2021](https://blogs.sussex.ac.uk/psychology/2021/08/17/running-cognitive-tasks-online-for-free/)

### Inferences
- Example budget: 100 participants × 15 min at $12/hr = $3.00 each, or $300 in rewards. Adding the 33.3% academic fee gives about $400. At the $8/hr floor, the same study is about $267. Hosting on Cognition.run or JATOS adds $0, and Gorilla would add about £75–£150.
- Solo-feasible, portfolio-worthy designs that fit a psych and stats background:
  - Pre-registered direct replications of classic cognitive effects (Stroop, flanker, attentional blink, serial dependence) with power analysis.
  - Psychometric reliability studies of online tasks, using split-half or ICC.
  - Many-labs-style contributions.
  - Pairing a behavioral task with the Muse ERP paradigm on oneself as a non-generalizable pilot.
- Pre-registration on OSF plus an open jsPsych repo on GitHub makes even a small study a credible portfolio piece.

### Gaps
- I could not confirm whether BU holds a Pavlovia or Gorilla institutional license. Check with BU Psychological & Brain Sciences or BU IT.
- I could not confirm whether Prolific requires proof of ethics approval at study launch.
- The current Gorilla student pricing page was not retrieved. The figures above conflict.

---

## 3. Open datasets for analysis-only projects (OpenNeuro, Allen, HCP, NeuroVault, UK Biobank, DANDI) and what strong student projects look like

### Takeaway
Analysis-only projects are the lowest-risk, highest-return path for a statistics-strong student. OpenNeuro (BIDS EEG/MEG/MRI), DANDI (NWB electrophysiology), and the Allen Brain Observatory (via AllenSDK) are free. HCP Open Access only requires registering and accepting data-use terms. UK Biobank has a student tier at £500 + VAT that requires a named supervisor and about 15 weeks of processing. HCP explicitly says your institution's IRB rules still apply, so get a BU "not human subjects research" or exempt determination before publishing.

### Cited Findings
- **OpenNeuro** [OLDER count, ~2021]: shared more than 600 datasets with data from more than 20,000 participants. It is a BRAIN Initiative archive organized around BIDS, following FAIR principles. — [Markiewicz et al., The OpenNeuro resource (PMC)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8550750/)
- **DANDI:** a BRAIN Initiative archive for neurophysiology data in NWB format, free for published datasets. License terms are set per Dandiset and must be checked on each record. [OLDER] An early abstract reported over 370 TB across 172+ datasets from 6 species. — [ConductScience DANDI vs OpenNeuro](https://conductscience.com/sciencedex/datasets/compare/dandi-nwb-vs-openneuro); [INCF](https://neuroinformatics.incf.org/node/357)
- **Allen Brain Observatory / AllenSDK:** open-source code to read and process Brain Observatory, Cell Types, and Connectivity Atlas data. Data come as NWB files. The SDK can download experiments by cortical area, imaging depth, and Cre line. Datasets include Visual Coding – Neuropixels (October 2019, passively viewing mice) and Visual Behavior – Neuropixels (release date shown as July 2022 in one docs version, "coming soon" in another). — [AllenSDK docs](https://allensdk.readthedocs.io/en/latest/index.html)
- **Human Connectome Project (HCP Young Adult):** Open Access data (all imaging, most behavioral) is available to anyone who registers on ConnectomeDB and accepts the Open Access Data Use Terms. Institutional rules still apply ("you may need IRB or ethics approval"). HCP data are not considered fully de-identified. Redistribution is allowed only under the same terms, with acknowledgment. Restricted data (exact age, family/twin structure, race/ethnicity, handedness, drug tests) needs an individual application with a named PI. — [HCP Data Use Terms](https://humanconnectome.org/study/hcp-young-adult/data-use-terms); [HCP open vs restricted quick reference](https://humanconnectome.org/study/hcp-young-adult/document/quick-reference-open-access-vs-restricted-data); [HCP restricted data usage](https://humanconnectome.org/study/hcp-young-adult/document/restricted-data-usage)
- **UK Biobank student tier:** a discounted data-only access fee of £500 + VAT for one project. It is open to students working toward a BSc, MSc, MD, PhD, or similar, but not postdocs or employees. Student and supervisor must both be on the application. The resulting publication must be student-authored. Access lasts 3 years from approval. Data release takes about 15 weeks from submission. — [UK Biobank financial support](https://www.ukbiobank.ac.uk/use-our-data/fees/financial-support/); [UKB FAQ: student fee](https://community.ukbiobank.ac.uk/hc/en-gb/articles/28612614071709-I-m-a-student-do-I-qualify-for-a-reduced-access-fee)
- **Model of a portfolio-grade student-style output:** Krigolson et al. published their Muse validation with open-source analysis code and replication instructions. Cannard et al. posted theirs as a bioRxiv preprint. — [Krigolson 2017 (PMC)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5344886/); [Cannard bioRxiv](https://www.biorxiv.org/content/10.1101/2021.11.02.466989.full.pdf)
- **Undergraduate outlet:** IMPULSE is an online undergraduate neuroscience journal. Submissions are rolling, reviewed by students under faculty guidance, and published immediately on acceptance. It is affiliated with the South Carolina Honors College. One listing names Appalachian State as publisher, so confirm. — [WFU IMPULSE Review Team](https://neuroandsociety.wfu.edu/wfu-impulse-review-team/); [Editage listing](https://www.editage.com/research-solutions/journal/impulse-the-premier-undergraduate-neuroscience-journal/40533)

### Inferences
- Solid analysis-only projects for this profile:
  1. Reanalyze an OpenNeuro EEG dataset (e.g., oddball or resting-state) with a pre-registered, multiverse, or robustness analysis, and publish it as a GitHub repo plus a PsyArXiv or bioRxiv preprint.
  2. Do a reliability or psychometrics study of HCP behavioral measures, a natural fit for a statistics background.
  3. Build an Allen Neuropixels decoding or tuning-curve analysis notebook.
  4. Write a small open-source tool, such as a cleaner Muse/Mind Monitor-to-BIDS converter or a QC dashboard.
  5. Treat a NeurIPS-style EEG challenge dataset (Section 6) as an analysis project.
- UK Biobank is feasible only with a BU faculty supervisor. The £500 + VAT fee and ~15-week lead time make it a semester-plus commitment. It is better suited to a UROP or thesis than a weekend project.
- Because HCP warns its data are not fully de-identified, and IRB rules may apply, ask BU's IRB for a written determination before submitting any reanalysis for publication. It is usually quick.

### Gaps
- NeuroVault was not specifically researched. I have no citable details on its access terms or size.
- I found no current 2026 dataset counts for OpenNeuro or DANDI. The figures above are dated.
- I could not confirm whether the Allen Brain Observatory has explicit terms of use beyond the historical public release.

---

## 4. Ethics and law: when IRB is needed, independent IRBs, consent, neural-data privacy laws, and animal work at home

### Takeaway
Under the Common Rule, IRB review is required when an activity is both "research" (a systematic investigation designed to contribute to generalizable knowledge) and involves "human subjects." Purely educational demos usually are not research. Results you intend to publish or present outside class are. Major institutions also require prior IRB review of self-experimentation, and investigators should not self-certify exemption. As a BU student, the realistic route is the BU IRB with a faculty sponsor; unaffiliated researchers must pay a fee-based or independent IRB.

On privacy: Colorado (2024), California (2024, effective 2025), Montana (2025), and Connecticut (effective July 1, 2026) treat neural data as sensitive. Massachusetts has a pending neural-data bill (H.103), and its broader privacy act sits in conference committee as of June 2026. Insects fall outside the federal Animal Welfare Act and PHS Policy, but vertebrate work at home is off-limits in practice.

### Cited Findings

**IRB triggers (Common Rule framework, via university guidance)**
- A project requires IRB review only if it meets both the federal definition of research and the federal definition of human subjects. An assignment designed only to teach methods is not a "systematic investigation designed to develop or contribute to generalizable knowledge." — [Ohio University class projects guidance](https://www.ohio.edu/research/compliance/human-subjects/classprojects)
- "Generalizable knowledge" means information with relevance beyond the population studied, or information added to the scientific literature. Determinations must be made by compliance staff, not individual researchers. — [UNT student research guidance](https://research.unt.edu/support-units/research-integrity-and-compliance/human-subjects-irb/student-research-guidance.html)
- Class assignments may become subject to IRB review if the faculty member or students change plans and use the data for research, during or after collection. — [UMich student research policy 2004 [OLDER]](https://online225.psych.wisc.edu/wp-content/uploads/225-Master/225-UnitPages/Unit-11/UMichigan_StudentResearch_2004.pdf)
- Classroom results presented in class or at a campus event are generally fine. Publishing or presenting externally is not. — [Boise State research compliance](https://boisestate.edu/research-compliance/?p=2841); [Tennessee Tech](https://ouweb.tntech.edu/research/humansubjects/irb-student-activities.php)
- Theses and dissertations usually meet the definition of research. — [ABAC IRB classroom vs research](https://abac.edu/_documents/provost/irb-classroom-activities-vs-research.pdf)
- An activity does not stop being "research" just because it happens in a classroom. — [Utah State classroom research](https://research.usu.edu/irb/classroom)

**Self-experimentation**
- Federal regulations do not distinguish self-experimentation from research on recruited subjects. Johns Hopkins, Northwestern, the University of Washington, and Boston Children's Hospital require prior IRB review before an investigator experiments on themselves. — [Johns Hopkins IRB: self-experimentation](https://www.hopkinsmedicine.org/institutional-review-board/guidelines-policies/guidelines/self-experimentation); [Northwestern IRB](https://irb.northwestern.edu/resources-guidance/investigator-manual/can-i-participate-in-my-own-research.html); [Boston Children's policy](https://test.childrenshospital.org/sites/default/files/2022-03/irbm-009-010-self-experimentation.pdf)
- A COPE case involved a single-author self-experiment submitted without ethics approval. The author argued that requiring approval would exclude independent researchers' self-experiments from publication. Journal policies vary. — [COPE case](https://publicationethics.org/node/18346)

**Exemption and independent IRBs**
- Federal agencies recommend that exempt determinations be made by someone not affiliated with the research. Investigators should not self-determine exemption. Some exempt categories require "limited IRB review." — [MedStar exempt pathway](https://www.medstarhealth.org/blog/exempt-human-subjects-research-pathway-to-approval); [WCG: IRB exemption](https://www.wcgclinical.com/insights/irb-exemption/)
- Unaffiliated researchers can use fee-based university IRBs. For example, the University of Nevada, Reno reviews external proposals, including exempt ones, on a fee schedule. Costs for affiliated researchers are usually absorbed by the institution. Unaffiliated researchers may pay out of pocket. — [UNR policy 501](https://www.unr.edu/research-integrity/human-research/human-research-protection-policy-manual/501-requirements-for-external-investigator-to-use-the-university-irb); [CASRAI IRB cost guide](https://www.casrai.org/guides/irb-approval-cost)

**Neural-data privacy law**
- **Colorado HB 24-1058**, signed April 17, 2024 (effective August 2024), added neural data to the Colorado Privacy Act's "sensitive data," which requires consent to collect. — [Blank Rome](https://blankrome.com/publications/colorado-becomes-first-state-explicitly-protect-neural-data); [Baker Hostetler](https://www.bakerlaw.com/insights/colorado-and-california-get-ahead-of-neural-data-regulation)
- **California SB 1223**, signed September 2024 (effective January 1, 2025), added neural data to CCPA "sensitive personal information." Its definition is narrower and excludes data inferred from non-neural information. It covers employee data. — [Sheppard Mullin](https://www.sheppard.com/insights/blogs/california-joins-colorado-in-the-brain-wave-action); [MoFo Q&A](https://www.mofo.com/pdf/resources/insights/241011-a-mofo-privacy-minute-q-a-california-revises-ccpa)
- **Montana SB 163**, signed May 2025, added neurotechnology data to the Genetic Information Privacy Act and defined "mental augmentation." One source gives an effective date of October 2025. **Connecticut SB 1295**, signed June 24, 2025, amends the CTDPA to treat neural data as sensitive. Its main provisions take effect July 1, 2026. — [LexisNexis State Net](https://www.lexisnexis.com/community/insights/legal/capitol-journal/b/state-net/posts/legislation-regulating-neural-data-picks-up-steam); [Neurorights Foundation](https://www.neurorightsfoundation.org/advocacy/united-states)
- **Federal MIND Act (S.2925)**, introduced September 2025 by Sens. Cantwell, Schumer, and Markey, would direct the FTC to study neural-data protection. As of January 2026 it remained in Senate Commerce with no further action. Later status is unconfirmed. — [Davis Wright Tremaine](https://www.dwt.com/blogs/privacy--security-law-blog/2025/10/senate-mind-act-neural-data-ftc-regulation); [Senate Commerce](https://www.commerce.senate.gov/?p=42489)
- **Massachusetts H.103 (Neural Data Privacy Protection Act)**, filed by Reps. Andres Vargas and Simon Cataldo and referred to the Advanced IT committee. It would require explicit informed consent to collect or process neural data, treat neural data as sensitive, and give access, correction, and deletion rights. The committee accompanied a new draft, H4746, on November 17, 2025. — [malegislature.gov H.103](https://malegislature.gov/Bills/194/H103); [MoFo](https://www.mofo.com/resources/insights/250317-more-states-propose-privacy-laws-safeguarding-neural-data)
- **Massachusetts Data Privacy Act:** the Senate passed S.2619 unanimously on September 25, 2025. The House passed its version unanimously in early June 2026; sources give H.5472 or H.5479, on June 4 or 5. A conference committee was appointed June 11, 2026. Reported provisions include coverage of entities processing data of 100,000+ consumers, affirmative consent to sell or share sensitive data, and a ban on selling precise geolocation. No source confirms that the final bill includes neural data, or that it has been enacted as of October 2026. — [Foley Hoag, June 2026](https://foleyhoag.com/news-and-insights/blogs/state-ag-insights/2026/june/one-step-closer-to-a-massachusetts-data-privacy-law-comparing-the-current-house-and-senate-bills/); [Charlestown Bridge, June 12 2026](https://charlestownbridge.com/2026/06/12/massachusetts-house-passes-landmark-data-privacy-legislation-with-strong-consumer-protections/); [malegislature.gov S.2619](https://malegislature.gov/bills/194/s2619)
- Risk Management magazine (Feb 2026) gives an overview of the new state neural-data law landscape. — [RM Magazine](https://www.rmmagazine.com/articles/article/2026/02/24/state-of-mind--the-new-landscape-of-neural-data-privacy-laws)

**Animal work**
- The federal Animal Welfare Act excludes invertebrates such as insects and crustaceans. Its "animal" definition is limited to warm-blooded species. PHS Policy covers all vertebrates but not invertebrates (cephalopods, insects, crustaceans). Some IACUCs, such as Michigan's, may not require review for non-cephalopod invertebrates. Cephalopods are treated differently. — [USF IACUC statutes](https://www.usf.edu/research-innovation/research-integrity-compliance/ric-programs/iacuc/statutes-regulations.aspx); [Animal Welfare Institute](https://awionline.org/content/online-guides-laws); [UMich animal care waiver](https://animalcare.umich.edu/protocol-approval/protocol-waiver/)

### Inferences
- A practical decision rule for this student:
  - **No IRB needed:** solo self-recording for personal learning, class demos that stay in class, and analysis of fully public, de-identified datasets. Even for public datasets, get a BU "not human subjects research" determination if you plan to publish.
  - **IRB needed (flag):**
    - Recording friends or roommates with EEG for a write-up.
    - Any Prolific or MTurk study intended for a poster, preprint, or journal.
    - Self-experiments you plan to publish.
    - Any study using HCP Restricted or UK Biobank data, which also require a supervisor and PI.
  - The cheapest compliant route is to find a BU faculty sponsor, through UROP or a lab, and submit through BU's IRB. Most minimal-risk EEG/behavioral studies likely qualify as exempt, but that call belongs to the IRB.
- The state neural-data laws mostly regulate businesses ("controllers") that meet thresholds; the Massachusetts bill's 100,000-consumer threshold is an example. A student running a small study is probably not directly covered. The laws matter in two ways: (a) the consumer apps you use (Muse, Emotiv, Neurosity) may send participants' EEG to company servers, which belongs in consent forms; (b) neurotech employers increasingly need privacy-literate staff. That makes them a good portfolio talking point. This applicability conclusion is an inference, not legal advice.
- For consent with consumer EEG, disclose: what is recorded, where the data go (local vs. vendor cloud), retention, sharing (e.g., OpenNeuro upload), and withdrawal. This mirrors the consent-and-access rights in H.103.
- At home, keep animal work to invertebrate prep that is widely used in teaching, such as the SpikerBox cockroach leg, using anesthesia and humane handling. Avoid RoboRoach-style live implantation if aiming for reputational safety. Never do vertebrate experiments at home.
- Do not do DIY brain stimulation (tDCS), given the safety concerns and lack of FDA review noted in Section 1.

### Gaps
- No BU-specific IRB pages were retrieved: BU's policy on class projects, student-initiated research, or "not human subjects research" determinations. Check BU's Office of Human Research Affairs or IRB site directly.
- I found no specific dollar figures for independent IRB review (e.g., WCG, Advarra) for an individual student.
- Massachusetts' state animal-cruelty statute as applied to invertebrates was not researched.
- The final status of the MA Data Privacy Act conference report, and whether neural data was folded in, could not be confirmed as of October 2026.
- OHRP's own text (45 CFR 46.102) was not fetched directly. The definitions above come from university guidance that paraphrases it.

---

## 5. At-home wet-lab limits in Massachusetts/Boston/Cambridge and Boston-area community labs

### Takeaway
Both Cambridge and Boston regulate recombinant DNA work by permit. Cambridge's ordinance covers individuals as well as organizations and requires NIH Guidelines compliance and a Cambridge Biosafety Committee permit. Boston requires a BPHC permit for rDNA work at BSL-2. Home genetic engineering is therefore effectively out for a student. The legal, low-cost option is BosLab, a volunteer-run BSL-1 community lab now in Somerville (Boynton Yards). It costs about $50–$60/month, with sponsored memberships available. At-home "neuroscience" should stay non-wet: electrophysiology kits, behavior, and data analysis.

### Cited Findings
- **Cambridge Chapter 8.20 (recombinant DNA ordinance):** all rDNA use in the city must strictly follow the NIH Guidelines, the chapter's requirements, and the Health Commissioner's regulations. The definition of "person" includes individuals and groups. Work requires a permit and a meeting with the Cambridge Biosafety Committee. Renewal fees are tiered by facility size, starting at $300 for up to 10,000 sq ft. Experiments above a certain NIH containment level are not permitted in the city. — [Cambridge rDNA ordinance (PDF)](https://www.cambridgepublichealth.org/wp-content/uploads/2022/08/Recombinant-DNA-Ordinance-Cambridge-MA.pdf); [Cambridge Biosafety Committee policies, 2017 update](https://www.cambridgepublichealth.org/wp-content/uploads/2022/08/Cambridge-Biosafety-Committee-Policies-Procedures-2017-update-v1.pdf)
- **Boston:** rDNA oversight was folded into the BPHC Biological Laboratory Regulations (2006, amended 2019). The 1994 rDNA use regulation was rescinded. An entity doing rDNA work at BSL-2/ABSL-2 needs a BPHC permit before starting. Permits run through the end of February, with renewal due January 31. "Agent" includes any agent modified with rDNA unless exempted. Contact: BPHC Biosafety Office, 617-534-5965. [OLDER: the most recent documents found are 2019.] — [BPHC revised guidelines 2019](https://content.boston.gov/sites/default/files/file/2021/03/BPHC%20Revised%20Guidelines_Biological%20Laboratory%20Regulations_10.03.2019.pdf); [BPHC FAQ 2019](https://content.boston.gov/sites/default/files/file/2021/03/FAQs_Biological%20Lab%20Regulations%20and%20Guidelines_11_25_19.pdf); [BMC sample rDNA permit](https://www.bmc.org/sites/default/files/Research/rDNA-Permit-BPHC.pdf)
- **BosLab biosafety and focus:** a biosafety level 1 lab working mainly with non-pathogenic organisms such as yeast and E. coli. — [Wikipedia: BOSLab](https://en.wikipedia.org/wiki/Boston_Open_Source_Science_Laboratory)
- **BosLab location and programs (Sept 2025):** started in a Davis Square garage in 2009, was in Cambridge from 2019, and is now 1,300 sq ft in The Hive at Boynton Yards. It is volunteer-run. It offers classes, artist-in-residence, scientist-in-training, workforce-development, and entrepreneur programs. Membership costs $60/month. BosLab's own about page still lists a Harvey Street, Cambridge address, which is probably outdated. — [Cambridge Day, Sept 14 2025](https://www.cambridgeday.com/2025/09/14/somervilles-community-biology-lab-makes-science-accessible-and-affordable/); [BosLab about](https://www.boslab.org/about)
- **BosLab membership (official page):** $50/month, billed monthly. It includes lab access, equipment, shared consumables, class discounts, and Slack/email community. Anyone working in the lab must be a member, and the application includes a basic lab-skills check. Sponsored memberships are available (contact homosapiens@boslab.org). The site could not be fetched directly from this environment (DNS failure), so this comes from search snippets. — [BosLab participate](https://www.boslab.org/participate); [BosLab PayPal page](https://www.boslab.org/paypal)
- Addgene's blog profiles BosLab's community-science model. — [Addgene blog](https://blog.addgene.org/cultivating-community-science-at-boslab)

### Inferences
- The Cambridge ordinance's definition of "person" includes individuals, and Boston's rules cover rDNA-modified agents. A student should not do any genetic engineering, such as GFP transformation kits, at a residence in either city without first contacting the health department. Doing it at BosLab, under its BSL-1 policies, is the straightforward compliant alternative. (Inference: the rules are written for facilities, but nothing found exempts residences.)
- Non-rDNA, BSL-1-compatible activities remain fine at home: invertebrate electrophysiology (SpikerBox), plant electrophysiology, human surface biopotentials (EMG/ECG/EEG), and behavioral work.
- BosLab costs about $600–$720/year. It is a better neuroscience fit for molecular or biology skill-building, such as PCR, culturing, or microscopy, than for neuro per se. Its value for this user is mostly résumé-building wet-lab experience and community networking.

### Gaps
- No Massachusetts state-level rule specific to home labs was found. Somerville's own biosafety rules, which now matter since BosLab moved to Somerville, were not researched. A Banker & Tradesman article notes "cities take second look at lab safety rules," but its content was not retrieved.
- BosLab's current membership price ($50 vs $60) and class prices are unconfirmed.
- Other Boston-area neuro-relevant spaces were not covered: makerspaces for electronics such as Artisan's Asylum, university clubs, or the NeuroTechX Boston chapter. NeuroTechX lists a Boston chapter, but no current activity was found ([NeuroTechX listing](https://beta.motherbase.ai/company/73095-neurotechx/)).

---

## 6. Citizen science, competitions, courses, and paths to income or stronger job and internship applications

### Takeaway
The highest-leverage moves for 2026–27:
- **Neuromatch Academy** (July; apply around March; paid TA roles exist): a structured group research project and network.
- **BR41N.IO BCI hackathons** (free, with cash prizes of about $400–$1,000 per track).
- **Kaggle-style EEG competitions:** the 2024 HMS contest had a $50k pool. Good for a public leaderboard result and a GitHub write-up.
- **BU UROP stipends:** $750–$1,500 per semester or $7,000 for summer. These also solve the IRB/supervisor problem.

Citizen science (Eyewire, FlyWire) builds familiarity but not income.

### Cited Findings

**Courses**
- **Neuromatch Academy 2026:** the Computational Neuroscience course ran July 6–24, 2026. It is full-time, 3 weeks, live online, with pods of about 15 students and a TA, and includes group research projects. Deep Learning ran July 6–24; NeuroAI and Climate ran July 13–24. Applications closed mid-March 2026; sources say March 15 or March 22. Tuition is globally adjusted. TA roles are paid, full-time, temporary contracts. Prerequisites: Python (numpy, scipy, matplotlib), linear algebra, probability, basic statistics, calculus, and foundational neuroscience. — [Neuromatch: computational neuroscience](https://neuromatch.io/computational-neuroscience-course/); [Neuromatch 2026 info sessions](https://neuromatch.io/?p=1368)

**Hackathons and competitions**
- **BR41N.IO (g.tec):** the 2026 Spring School hackathon ran April 25–26, with games, software/art, and data-analysis tracks and 130–150+ teams. Another ran during IEEE SMC 2026, October 4–5, in Bellevue, WA. It is free and open to anyone, students included. Prizes conflict: the g.tec page says $1,000 / $600 / $400 per track, and the IEEE SMC BMI page says $600 / $400 / $200. — [g.tec IEEE SMC 2026 hackathon](https://www.gtec.at/hackathon/ieee-smc-2026/); [IEEE SMC BMI CFP](https://www.ieeesmc.org/bmi/wp-content/uploads/sites/28/2025/11/CFP-IEEE-SMC-2026-BMI.pdf); [SNNU Saarland team result](https://www.snnu.uni-saarland.de/?p=3011); [ISR Lisbon](https://isr.uc.pt/news/3rd-br41nio-hackathon)
- [OLDER, 2024] **Kaggle "HMS – Harmful Brain Activity Classification":** an EEG six-class classification task scored by KL divergence. It ran January 10 – April 9, 2024, had a $50,000 prize pool, and drew 2,767 teams. — [Albumentations competition record](https://albumentations.ai/adoption/competitions/kaggle/hms-harmful-brain-activity-classification/); [Nikkei announcement](https://www.nikkei.co.jp/nikkeiinfo/en/news/announcements/1215.html)
- **NeurIPS 2025 EEG Foundation Challenge:** cross-task and cross-subject zero-shot EEG decoding, plus psychopathology prediction. Its datasets remain useful for analysis projects. — [NeurIPS 2025 competition page](https://neurips.cc/virtual/2025/loc/san-diego/competition/127719); [arXiv description](https://arxiv.org/html/2506.19141v1)
- **PNPL 2026 competition (MEG, LibriBrain):** word-level decoding with a "Deep" within-subject track and a "Broad" cross-subject track. LibriBrain100 adds 32 subjects. Prize details were not found. — [AI Weekly](https://aiweekly.co/alerts/pnpl-2026-contest-advances-non-invasive-bci-to-word-decoding)
- **AI BCI Global Challenge (Shenzhen, 2026):** four tracks, including non-invasive and consumer BCI. Rewards appear to be accelerator access and investment, not cash. — [SuperScout listing](https://superscout.co/program/ai-bci-global-challenge-neurohub-accelerator)

**Citizen science**
- **Eyewire** (Seung Lab, launched 2012): about 350,000 players and 6,000 neurons traced as of March 2025. Player tracing also trains the AI. Eyewire II received a $950,000 Research to Prevent Blindness award (April 22, 2026) to map all cell types in the mouse retina. FlyWire is a successor using a more selective citizen-science model. — [Wikipedia: Eyewire](https://en.wikipedia.org/wiki/Eyewire); [RPB press release](https://www.rpbusa.org/news-press/research-to-prevent-blindness-award-to-enable-transformational-scientific-milestone-in-neuroscience-and-vision-science/); [FlyWire forum](https://discuss.flywire.ai/t/welcome-to-flywire/20)

**Paid research at BU**
- **BU UROP:**
  - Student Research Award: up to $750 per semester for 5 hrs/week, or $7,000 for summer (40 hrs/week, 10 weeks).
  - Faculty Matching Grant: up to $1,500 per semester for 10 hrs/week, with the mentor matching half.
  - Stipends are taxable. You cannot take academic credit and a stipend for the same research. Open to full-time BU undergraduates.
  - [OLDER, 2024] An earlier page listed a $6,000 summer amount.
  — [BU UROP funding & eligibility](https://www.bu.edu/urop/get-involved/funding-eligibility/); [BU Research announcement Aug 2025](https://www.bu.edu/research/2025/08/12/open-for-applications-undergraduate-research-opportunities-program-urop)

### Inferences
- **A coherent 12-month portfolio plan for this profile:**
  - **Fall 2026:** buy a Muse 2 + Mind Monitor (~$265). Replicate the Krigolson oddball P300 and alpha-blocking on yourself as a learning exercise, with no publication claims. Do an OpenNeuro reanalysis with a public GitHub repo.
  - **Spring 2027:** recruit a BU faculty mentor and apply for UROP. Turn the pilot into an IRB-approved small-N study, such as a test-retest reliability study of consumer-EEG alpha or P300. Apply to Neuromatch by mid-March.
  - **Ongoing:** enter BR41N.IO or Kaggle EEG challenges, and post write-ups as preprints or submit to IMPULSE.
- **Income paths in rough order of reliability:**
  1. UROP stipends.
  2. Paid Neuromatch TA roles, after completing the course.
  3. Hackathon prizes, which are modest and competitive.
  4. Kaggle prizes, which are large pools but very competitive.
  5. Freelance or contract EEG-analysis or data work. This is an inference; no sourced marketplace was found.
- **For job and internship applications** (neurotech startups, BCI companies, cognitive-science labs, UX/neuromarketing), these signal competence:
  - A pre-registered study.
  - A clean analysis repo using standard formats (BIDS/NWB) and tools (BrainFlow, AllenSDK).
  - A hackathon placement.
  - Familiarity with neural-data privacy law (Section 4).
  The psych and stats background is a differentiator for experimental design and inference, which many engineering-heavy BCI teams lack. This is an inference.

### Gaps
- Official 2026 Kaggle neuroscience competitions, and the official "BCI Competition" series status, were not found.
- Neuromatch 2026 tuition amounts and TA pay rates were not found.
- No 2026 Boston-area neurotech hackathons were found (e.g., MIT or Harvard neurotech clubs, NeuroTechX Boston). Current Boston NeuroTechX activity is unconfirmed.
- No sourced freelance market for EEG analysis was found.
- UROP eligibility applies to undergraduates. If the user is a graduate student, this path does not apply, and alternatives were not researched.
