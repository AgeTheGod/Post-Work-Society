#   Employment Analysis

This is where the bulk of the analysis should occur because there is a lot of noise and misinformation about "Employment" and who does what.

Those in employment (economically active) and those not in employment (economically inactive)

Employment itself we want to further break down into various categories such as...
- Those in productive employment (make something)
- vs. administrative employment
- vs. "value add" employment
- vs. public service employment
- vs. private service employment
- vs. not for profit employment

In fact there are many ways to slice & dice the data to focus on different aspects of "Employment" that I can think of.
Unfortunately although a lot of data is available e.g. via ONS, Eurostat, BLS, Statista, etc. most of it is...
1. preprocessed summary data
2. presented as pre-formatted static data so difficult to download and analyze
3. not necessarily classified in the way that I want it to be e.g. employment type by type of employer.
4. nearly always historical data that's at least 6 months out of date

Consequently, although we can get a general picture of how employment is distributed across the population we can't get accurate details due to reporting periods and data timing issues.

The bulk of this analysis was done using Google AI and the prompts and sources are included in the analysis below. 

##  United Kingdom Analysis

    Prompt: What is the standard industrial classification scheme used by the UK Office of National Statistics and what are the top level classifications in that scheme?

The framework used by the [UK Office for National Statistics (ONS)](https://www.ons.gov.uk/methodology/classificationsandstandards/ukstandardindustrialclassificationofeconomicactivities) is the UK Standard Industrial Classification of Economic Activities (UK SIC). [1]
The system provides a uniform, five-digit hierarchical layout designed to categorise businesses and organisations by the exact nature of their economic activities. The classification system is aligned with international systems, remaining structurally identical to the European NACE system up to the four-digit level, with an additional fifth digit added to track specific UK sub-classes. [1, 2, 3]
The 21 Top-Level Classifications
The top-level of the UK SIC consists of 21 sections (labeled A-U) representing broad industry groups, ranging from agriculture and manufacturing to public administration, education, and extraterritorial organisations. [4, 5, 6]

Hierarchical Structure
The system uses a five-step hierarchical breakdown to classify activities with increasing precision: [1, 4]

1. Sections (Letter): The 21 broad categories.
2. Divisions (2 Digits): Broad industrial sectors.
3. Groups (3 Digits): Narrower industry segments.
4. Classes (4 Digits): Specific international standard categories.
5. Sub-classes (5 Digits): Detailed UK-specific classifications.
   [2, 4, 7, 8, 9]


[1] [https://www.ons.gov.uk](https://www.ons.gov.uk/methodology/classificationsandstandards/ukstandardindustrialclassificationofeconomicactivities)
[2] [https://classification.codes](https://classification.codes/classifications/industry/uk-sic)
[3] [https://consultations.ons.gov.uk](https://consultations.ons.gov.uk/external-affairs/uk-sic-consultation/)
[4] [https://www.ons.gov.uk](https://www.ons.gov.uk/file?uri=/methodology/classificationsandstandards/ukstandardindustrialclassificationofeconomicactivities/uksic2007/uksic2007web.pdf)
[5] [https://www.ons.gov.uk](https://www.ons.gov.uk/filters/f097989b-1467-4478-b3ca-a34ed5763776/dimensions/unofficialstandardindustrialclassification)
[6] [https://www.thecompanywarehouse.co.uk](https://www.thecompanywarehouse.co.uk/assets/images/guides/setting-up-a-limited-company/SIC_codes_V2.pdf)
[7] [https://www.hesa.ac.uk](https://www.hesa.ac.uk/support/documentation/industrial/sic2007)
[8] [https://resources.companieshouse.gov.uk](https://resources.companieshouse.gov.uk/sic/)
[9] [https://classification.codes](https://classification.codes/classifications/industry/uk-sic)

### UK Employment Breakdown by SIC Industry Sector

    Prompt: Summarize employment numbers grouped by those top level classifications

The [Office for National Statistics (ONS)](https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/jobsandvacanciesintheuk/may2026) tracks total UK employment across these sections using the Workforce Jobs (WFJ) dataset. As of the latest primary quarterly updates, the total UK workforce stands at approximately 36.6 million jobs. [1]
The ONS officially groups the 21 top-level SIC sections into 19 standard reporting sectors for labor market analysis (combining Sections D and E, and Sections T and U due to smaller workforce sizes). [1, 2]

| UK SIC Code & Top-Level Classification Section [2, 3, 4] | Broad Industry Sector Description | Approximate Jobs / Share of UK Workforce |
|---|---|---|
| Q | Human health and social work activities | ~4.9 million (Largest single sector) |
| G | Wholesale and retail trade; repair of motor vehicles | ~4.6 million |
| P | Education | ~3.4 million |
| M | Professional, scientific and technical activities | ~3.3 million |
| N | Administrative and support service activities | ~3.0 million |
| C | Manufacturing | ~2.6 million |
| F | Construction | ~2.3 million |
| I | Accommodation and food service activities | ~2.4 million |
| H | Transportation and storage | ~1.8 million |
| O | Public administration and defence; compulsory social security | ~1.6 million |
| K | Financial and insurance activities | ~1.1 million |
| J | Information and communication | ~1.0 million |
| R | Arts, entertainment and recreation | ~1.0 million |
| S | Other service activities | ~0.9 million |
| L | Real estate activities | ~0.6 million |
| A | Agriculture, forestry and fishing | ~0.4 million |
| D & E | Electricity, gas, steam, water supply & waste management | ~0.4 million |
| B | Mining and quarrying | ~0.06 million |
| T & U | Households as employers; extraterritorial organisations | ~0.05 million |

#### Macro Workforce Groupings
To understand the macroeconomic environment at a broader glance, the ONS often filters these numbers into three overriding divisions:

* The Services Sector (Sections G–U): Dominates the UK labor market, capturing roughly 83% to 85% of all active workforce jobs.
* Public & Social Infrastructure (Sections O, P, Q): Combined public administration, health, and education represent over 32% of the total workforce.
* Production & Construction (Sections A–F): Manufacturing, building trades, agriculture, and energy sectors make up the remaining ~15% of national employment. [4, 5]

[1] [https://backup.ons.gov.uk](https://backup.ons.gov.uk/wp-content/uploads/sites/3/2026/05/Vacancies-and-jobs-in-the-UK-May-2026.pdf)
[2] [https://www.ons.gov.uk](https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/employeesintheukbyindustry/2023)
[3] [https://www.ons.gov.uk](https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/jobsandvacanciesintheuk/may2026)
[4] [https://www.ons.gov.uk](https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/industryandoccupationenglandandwales/census2021)
[5] [https://www.ethnicity-facts-figures.service.gov.uk](https://www.ethnicity-facts-figures.service.gov.uk/work-pay-and-benefits/employment/employment-by-sector/latest)
[6] [https://www.ons.gov.uk](https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/uklabourmarket/march2025/relateddata?q=&limit=10&sort=title&page=7)

### UK Employment Share vs. Percentage of GVA/GDP by SIC Sector [2]

    Prompt: Include percentage of GDP along with the employment numbers

The [Office for National Statistics (ONS)](https://www.ons.gov.uk/economy/grossdomesticproductgdp/compendium/unitedkingdomnationalaccountsthebluebook/2025/theindustrialanalysis) measures economic output at the industry level using Gross Value Added (GVA). GVA tracks the exact value of goods and services produced minus intermediate costs, matching Gross Domestic Product (GDP) when combined with taxes and minus product subsidies. [1, 2]
The table below correlates the [ONS Workforce Jobs dataset](https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/jobsandvacanciesintheuk/may2026) with the primary ONS industry output data to show the relationship between employment volume and economic weight. [3]

| UK SIC Code [2, 4, 5, 6, 7] | Broad Industry Sector Description | Workforce Jobs (Total) | Share of UK Workforce | Share of National GVA / GDP |
|---|---|---|---|---|
| Q | Human health and social work activities | ~4.9 million | 13.4% | 8.5% |
| G | Wholesale and retail trade; motor repair | ~4.6 million | 12.6% | 9.9% |
| P | Education | ~3.4 million | 9.3% | ~6.0% |
| M | Professional, scientific & technical | ~3.3 million | 9.0% | 8.3% |
| N | Administrative and support services | ~3.0 million | 8.2% | ~5.3% |
| C | Manufacturing | ~2.6 million | 7.1% | 9.1% |
| I | Accommodation and food services | ~2.4 million | 6.6% | ~3.0% |
| F | Construction | ~2.3 million | 6.3% | ~6.0% |
| H | Transportation and storage | ~1.8 million | 4.9% | ~4.5% |
| O | Public administration & defence | ~1.6 million | 4.4% | ~4.4% |
| K | Financial and insurance activities | ~1.1 million | 3.0% | 8.8% |
| J | Information and communication | ~1.0 million | 2.7% | ~7.0% |
| R | Arts, entertainment and recreation | ~1.0 million | 2.7% | ~1.7% |
| S | Other service activities | ~0.9 million | 2.5% | ~2.0% |
| L | Real estate activities | ~0.6 million | 1.6% | 13.1% |
| A | Agriculture, forestry and fishing | ~0.4 million | 1.1% | 0.7% |
| D & E | Energy, utilities & waste management | ~0.4 million | 1.1% | ~3.4% |
| B | Mining and quarrying | ~0.06 million | 0.2% | ~1.0% |
| T & U | Private households & extraterritorial | ~0.05 million | 0.1% | <0.2% |

#### Key Structural Insights

* The Real Estate Disconnect: Section L (Real Estate) exhibits the largest disparity between labor and monetary output, generating 13.1% of national GVA while utilizing just 1.6% of the workforce. This is driven heavily by ONS capital calculations, which include the "imputed rental value" of owner-occupied housing.
* High Productivity Service Sectors: Finance (8.8% GVA vs 3.0% jobs) and Information/Tech (~7.0% GVA vs 2.7% jobs) punch far above their weight in direct economic output per worker.
* Labor-Intensive Foundations: Healthcare (Section Q) and Education (Section P) demand a combined 22.7% of all UK jobs, but represent roughly 14.5% of absolute GVA, reflecting the high-employment nature of public sector infrastructure. [2, 3, 4]

[1] [https://www.nomisweb.co.uk](https://www.nomisweb.co.uk/datasets/gvasa)
[2] [https://commonslibrary.parliament.uk](https://commonslibrary.parliament.uk/research-briefings/cbp-8353/)
[3] [https://www.ons.gov.uk](https://www.ons.gov.uk/economy/grossdomesticproductgdp/compendium/unitedkingdomnationalaccountsthebluebook/2025/theindustrialanalysis)
[4] [https://www.ciip.group.cam.ac.uk](https://www.ciip.group.cam.ac.uk/innovation/structure-and-performance-of-the-uk-economy-25/)
[5] [https://www.ons.gov.uk](https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/industryandoccupationenglandandwales/census2021)
[6] [https://www.ons.gov.uk](https://www.ons.gov.uk/economy/grossdomesticproductgdp/bulletins/gdpmonthlyestimateuk/september2025)
[7] [https://www.gov.uk](https://www.gov.uk/government/statistics/business-population-estimates-2025/business-population-estimates-for-the-uk-and-regions-2025-statistical-release)
[8] [https://researchbriefings.files.parliament.uk](https://researchbriefings.files.parliament.uk/documents/CBP-8353/CBP-8353.pdf)

## 10-Year UK Employment Change by SIC Industry Sector

    Prompt: Include the percentage change in the UK employment numbers comnpared to 10 years ago

The total number of UK workforce jobs has grown by approximately 6.4% over the last decade, climbing from around 34.4 million in early 2016 to [36.6 million today](https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/jobsandvacanciesintheuk/march2026).
However, this growth has been unevenly spread. The structural shift toward a technology, knowledge, and health-driven economy has caused massive job expansion in specific sectors, while brick-and-mortar retail and heavy production have contracted or flattened. [1, 2, 3]

| UK SIC Code [1, 4, 5, 6, 7] | Broad Industry Sector Description | Current Jobs (2026) | Est. Jobs (2016) | 10-Year % Change in Headcount |
|---|---|---|---|---|
| J | Information and communication | ~1.6 million | ~1.25 million | +28.0% (Fastest growth) |
| M | Professional, scientific & technical | ~3.4 million | ~2.75 million | +23.6% |
| Q | Human health and social work activities | ~5.0 million | ~4.15 million | +20.5% |
| L | Real estate activities | ~0.7 million | ~0.60 million | +16.7% |
| O | Public administration & defence | ~1.8 million | ~1.55 million | +16.1% |
| I | Accommodation and food services | ~2.4 million | ~2.20 million | +9.1% |
| P | Education | ~3.1 million | ~2.90 million | +6.9% |
| F | Construction | ~2.3 million | ~2.20 million | +4.5% |
| N | Administrative and support services | ~3.0 million | ~2.90 million | +3.4% |
| H | Transportation and storage | ~1.9 million | ~1.85 million | +2.7% |
| R | Arts, entertainment and recreation | ~1.1 million | ~1.08 million | +1.8% |
| S & T | Other service activities & private households | ~1.0 million | ~0.99 million | +1.0% |
| D & E | Energy, utilities & waste management | ~0.4 million | ~0.40 million | 0.0% (Flat) |
| A | Agriculture, forestry and fishing | ~0.34 million | ~0.35 million | -2.8% |
| C | Manufacturing | ~2.5 million | ~2.65 million | -5.6% |
| G | Wholesale and retail trade; motor repair | ~4.6 million | ~4.95 million | -7.1% |
| K | Financial and insurance activities | ~1.1 million | ~1.22 million | -9.8% |
| B | Mining and quarrying | ~0.05 million | ~0.06 million | -16.7% (Sharpest decline) |

### Key Decadal Workforce Trends

* The White-Collar & Tech Boom: Sections J (Tech/Media) and M (Professional/Scientific) exploded, adding a combined one million net new jobs [over the last decade](https://www.ons.gov.uk/economy/nationalaccounts/uksectoraccounts/compendium/economicreview/april2019/longtermtrendsinukemployment1861to2018). This mirrors the heavy corporate digitisation and the rapid scaling of the UK software, consulting, and legal sectors.
* The Retail Retraction: Section G (Wholesale & Retail) shed roughly 350,000 jobs. This structural decline highlights the dramatic transition from physical brick-and-mortar storefronts to automated logistics and e-commerce platforms.
* The Corporate Shrinkage of Finance: Despite the UK remaining a dominant global financial hub, Section K (Banking & Insurance) shed nearly 10% of its workforce. This shrinkage is primarily due to intensive automation, algorithmic trading, and the widespread closure of physical bank branches across high streets.
* The State-Backed Expansion: Driven by demographic aging and post-pandemic demands, the Health and Social Care sector (Section Q) scaled drastically, adding nearly 850,000 workers to its total ranks since 2016.

[1] [https://www.statista.com](https://www.statista.com/statistics/281998/employment-figures-in-the-united-kingdom-uk/)
[2] [https://commonslibrary.parliament.uk](https://commonslibrary.parliament.uk/research-briefings/cbp-9366/)
[3] [https://www.ciip.group.cam.ac.uk](https://www.ciip.group.cam.ac.uk/innovation/structure-of-the-uk-economy/)
[4] [https://researchbriefings.files.parliament.uk](https://researchbriefings.files.parliament.uk/documents/CBP-9366/CBP-9366.pdf)
[5] [https://www.ons.gov.uk](https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/jobsandvacanciesintheuk/may2026)
[6] [https://cy.ons.gov.uk](https://cy.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/bulletins/jobsandvacanciesintheuk/may2026)
[7] [https://backup.ons.gov.uk](https://backup.ons.gov.uk/wp-content/uploads/sites/3/2026/05/Vacancies-and-jobs-in-the-UK-May-2026.pdf)

## 10-Year Change in Percentage Share of UK Workforce Jobs

    Prompt: Convert the number of jobs to a percentage of jobs

To make comparing industry sizes easier, the absolute workforce figures have been converted directly into percentage shares. This highlights exactly where the largest movements occurred over the last 10 years.
While the total UK labor market expanded by over 2.2 million net jobs since 2016 [34.4m to 36.6m], the relative "slice of the pie" shrank for traditional sectors like retail and finance while expanding for tech and healthcare.

| UK SIC Code | Broad Industry Sector Description | 2016 Share of Total Jobs | 2026 Share of Total Jobs | Percentage Point (pp) Shift |
|---|---|---|---|---|
| Q | Human health and social work activities | 12.1% | 13.7% | +1.6 pp (Largest share gain) |
| M | Professional, scientific & technical | 8.0% | 9.3% | +1.3 pp |
| J | Information and communication | 3.6% | 4.4% | +0.8 pp |
| O | Public administration & defence | 4.5% | 4.9% | +0.4 pp |
| L | Real estate activities | 1.7% | 1.9% | +0.2 pp |
| I | Accommodation and food services | 6.4% | 6.6% | +0.2 pp |
| F | Construction | 6.4% | 6.3% | -0.1 pp |
| P | Education | 8.4% | 8.5% | +0.1 pp |
| R | Arts, entertainment and recreation | 3.1% | 3.0% | -0.1 pp |
| S & T | Other service activities & private households | 2.9% | 2.7% | -0.2 pp |
| D & E | Energy, utilities & waste management | 1.2% | 1.1% | -0.1 pp |
| H | Transportation and storage | 5.4% | 5.2% | -0.2 pp |
| A | Agriculture, forestry and fishing | 1.0% | 0.9% | -0.1 pp |
| N | Administrative and support services | 8.4% | 8.2% | -0.2 pp |
| B | Mining and quarrying | 0.2% | 0.1% | -0.1 pp |
| K | Financial and insurance activities | 3.5% | 3.0% | -0.5 pp |
| C | Manufacturing | 7.7% | 6.8% | -0.9 pp |
| G | Wholesale and retail trade; motor repair | 14.4% | 12.6% | -1.8 pp (Largest share loss) |

## Key structural insights from the percentages

* The Twin Drivers: Healthcare (Section Q) and Professional/Scientific Corporate Services (Section M) were the primary engines of UK job structural evolution, expanding their combined share of national employment by 2.9 percentage points.
* The Retail Eclipse: In 2016, Wholesale and Retail (Section G) was indisputably the largest employer in the UK at 14.4%. Over the decade, its structural footprint shrank so heavily (-1.8 pp) that it has been completely overtaken by Healthcare as the country's largest source of employment.
* The Manufacturing Drift: Manufacturing (Section C) continued its long-term structural decline, slipping from nearly 8% of all UK jobs down to just 6.8%.


##  European Union Analysis

### EU Employment Share vs. Percentage of GVA/GDP by NACE Sector

    Prompt: Do the same analysis for the European Union

The European Union uses the Statistical Classification of Economic Activities in the European Community (NACE). Because the UK SIC system was derived from NACE, the structural layout is virtually identical. [1, 2, 3, 4]
Eurostat tracks total EU employment (approximately 219 million workers) and economic output via Gross Value Added (GVA). 

To prevent cognitive data fatigue, Eurostat standardises its high-level public reporting into 10 aggregated macro-sectors (the NACE A*10 breakdown), grouping the 21 individual letters. [1, 2, 3, 5]

| NACE Aggregated Code & Sections [2, 3, 6, 7, 8] | Broad Industry Sector Description | Approximate Employment | Share of EU Workforce | Share of EU Gross Value Added |
|---|---|---|---|---|
| G, H, I | Wholesale, retail, transport, accommodation & food | ~53.5 million | 24.4% | 19.1% |
| O, P, Q | Public admin, defence, education, health & social work | ~51.3 million | 23.4% | 18.4% |
| C (plus B, D, E) | Industry (with Manufacturing taking 30m+ jobs) | ~34.8 million | 15.9% | 20.1% |
| M & N | Professional, scientific, technical & admin services | ~26.1 million | 11.9% | 11.5% |
| F | Construction | ~14.5 million | 6.6% | 5.3% |
| A | Agriculture, forestry and fishing | ~10.5 million | 4.8% | 1.7% |
| J | Information and communication | ~7.8 million | 3.6% | 5.5% |
| K | Financial and insurance activities | ~5.8 million | 2.6% | 4.6% |
| L | Real estate activities | ~2.8 million | 1.3% | 10.3% |
| R, S, T, U | Arts, entertainment, recreation & other services | ~12.1 million | 5.5% | 3.5% |

#### Critical Variations: EU vs. UK Economic Structures

* The Manufacturing Core: The most glaring difference is the industrial core. In the EU, Industry / Manufacturing represents over 20% of all economic value and nearly 16% of jobs, heavily sustained by manufacturing powerhouses like [Germany (where manufacturing is ~20% of GVA)](https://www.destatis.de/Europa/EN/Topic/Industry-trade-services/Industry_GVA.html), Poland, and Czechia. In contrast, the UK manufacturing sector accounts for under 10% of GVA and 7% of its workforce.
* Agriculture Retention: The EU maintains a much larger agricultural footprint, employing 4.8% of the workforce (~10.5 million people) compared to the UK's minor 1.1% agricultural labor allocation.
* Hyper-Productive Niches: Much like the UK, NACE Section L (Real Estate) exhibits massive asset-driven economic weight, claiming 10.3% of GVA with only 1.3% of active labor. Information and Communication (Tech) also shows strong efficiency, delivering 5.5% of absolute GVA using only 3.6% of total headcount. [2, 3, 5, 9, 10, 11]

[1] [https://www.indexbox.io](https://www.indexbox.io/blog/eurostat-releases-2024-2025-gross-value-added-data-by-industry/)
[2] [https://www.weforum.org](https://www.weforum.org/stories/2023/02/eu-countries-largest-economies-energy-gdp/)
[3] [https://en.wikipedia.org](https://en.wikipedia.org/wiki/Economy_of_the_European_Union)
[4] [https://ec.europa.eu](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Quarterly_national_accounts_-_GDP_and_employment)
[5] [https://ec.europa.eu](https://ec.europa.eu/eurostat/databrowser/view/nama_10_a64_e/default/table?lang=en)
[6] [https://www.statista.com](https://www.statista.com/statistics/1195197/employment-by-sector-in-europe/)
[7] [https://ec.europa.eu](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=National_accounts_and_GDP)
[8] [https://ec.europa.eu](https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20221220-4)
[9] [https://ec.europa.eu](https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20241025-1)
[10] [https://www.destatis.de](https://www.destatis.de/Europa/EN/Topic/Industry-trade-services/Industry_GVA.html)
[11] [https://ec.europa.eu](https://ec.europa.eu/eurostat/databrowser/view/nama_10_a64/default/table)

### 10-Year Change in Percentage Share of the European Union Workforce

The total number of employed persons in the European Union has grown by approximately 6.9% over the last decade, climbing from around 185 million in 2016 to [197.7 million today](https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20260417-1).
Using Eurostat's standardized A*10 NACE reporting blocks, the absolute workforce data converts into clear percentage shares to highlight exactly how the continental labor market has evolved. [1]

| NACE Aggregated Sections | Broad Industry Sector Description | 2016 Share of EU Jobs | 2026 Share of EU Jobs | Percentage Point (pp) Shift |
|---|---|---|---|---|
| O, P, Q | Public admin, defence, education, health & social work | 22.9% | 23.9% | +1.0 pp (Largest share gain) |
| M & N | Professional, scientific, technical & admin services | 11.2% | 12.1% | +0.9 pp |
| J | Information and communication (Tech) | 3.1% | 3.8% | +0.7 pp |
| K | Financial and insurance activities | 2.5% | 2.6% | +0.1 pp |
| L | Real estate activities | 1.2% | 1.3% | +0.1 pp |
| R, S, T, U | Arts, entertainment, recreation & other services | 5.5% | 5.5% | 0.0 pp (Flat) |
| F | Construction | 6.5% | 6.4% | -0.1 pp |
| G, H, I | Wholesale, retail, transport, accommodation & food | 24.8% | 24.2% | -0.6 pp |
| C (plus B, D, E) | Industry (including Manufacturing) | 16.4% | 15.6% | -0.8 pp |
| A | Agriculture, forestry and fishing | 5.9% | 4.6% | -1.3 pp (Largest share loss) |

#### Key Decadal Trends Across the EU

* The Persistent Industrial Baseline: While Industry and Manufacturing (Sections B-E) dropped slightly by 0.8 percentage points, the EU still keeps 15.6% of its total workforce in industrial production. This remains more than double the structural weight of the UK, which sits at just 6.8%.
* The Rapid De-agriculturalization of Eastern Europe: Agriculture (Section A) saw the most severe decline, losing 1.3 percentage points of total EU labor allocation. This represents millions of workers shifting away from traditional farming—primarily in member states like Romania, Poland, and Greece—and moving into urban service or construction roles.
* The Rise of Digital and Scientific Services: Replicating the UK trend, the combined expansion of Information Tech (Section J) and Professional Corporate Services (Section M) added a massive 1.6 percentage point gain to total EU employment.
* State and Infrastructure Resilience: Public administration, healthcare, and education (Sections O-Q) expanded their baseline footprint to claim nearly a quarter of all jobs in the EU (23.9%), establishing this macro-sector as one of the most reliable and non-cyclical employers on the continent. [2, 3]

[1] [https://ec.europa.eu](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Employment_statistics_within_national_accounts)
[2] [https://ec.europa.eu](https://ec.europa.eu/eurostat/statistics-explained/index.php?wpacode=31303&title=Employment_statistics_within_national_accounts&etrans=es)
[3] [https://ec.europa.eu](https://ec.europa.eu/eurostat/statistics-explained/SEPDF/cache/62450.pdf)
[4] [https://ec.europa.eu](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Productivity_trends_using_key_national_accounts_indicators)

##  The USA

### 10-Year Share Change with Current Absolute Employment Numbers (USA)

    Pronpt: Do the same Job Percentage analysis for the USA including current employment numbers as additional column in analysis

To provide a complete view of the current landscape, the absolute headcount numbers have been re-introduced alongside the percentage shares.
Out of the total ~161.4 million jobs in the US economy today, the data highlights how absolute workforce volumes correlate with relative market share.

| NAICS Supersector Block | Broad Industry Sector Description | 2016 Share of US Jobs | 2026 Share of US Jobs | Percentage Point (pp) Shift | Current Headcount (2026) |
|---|---|---|---|---|---|
| Trade, Trans., & Utilities | Wholesale, Retail, Supply Chain, Logistics, & Utilities | 18.9% | 17.8% | -1.1 pp | ~28.7 million |
| Education & Health Services | Private Healthcare, Clinics, Nursing, & Private Schools | 15.6% | 16.8% | +1.2 pp | ~27.1 million |
| Professional & Business Services | Tech/Software, Legal, Consulting, Corporate Admin | 14.0% | 14.8% | +0.8 pp | ~23.9 million |
| Government | Local, State, and Federal Civil Services (inc. Public Education) | 15.4% | 14.3% | -1.1 pp | ~23.1 million |
| Leisure & Hospitality | Restaurants, Hotels, Casinos, Tourism, & Arts | 10.7% | 10.6% | -0.1 pp | ~17.1 million |
| Manufacturing | Aerospace, Automotive, Electronics, & Goods Production | 8.5% | 8.0% | -0.5 pp | ~12.9 million |
| Financial Activities | Investment Banking, Insurance, & Real Estate Agencies | 5.7% | 5.7% | 0.0 pp | ~9.2 million |
| Construction | Housing, Commercial Infrastructure, & Civil Projects | 4.6% | 5.1% | +0.5 pp | ~8.2 million |
| Other Services | Automotive Repair, Personal Care, Dry Cleaning, Advocacy | 3.9% | 3.7% | -0.2 pp | ~6.0 million |
| Information | Tech Giants, Silicon Valley SaaS, Streaming, Media, Telecom | 1.9% | 2.0% | +0.1 pp | ~3.2 million |
| Mining & Logging | Oil & Gas Extraction, Fracking, & Commercial Forestry | 0.5% | 0.4% | -0.1 pp | ~0.6 million |

#### Key Observations with Headcounts Included

* The Scale of Trade vs. Health: While Trade and Logistics lost structural share over the decade due to automation, it remains the largest employment engine in the United States with 28.7 million workers. However, Private Health and Education is rapidly closing the gap at 27.1 million workers.
* The "Information" Paradox: Silicon Valley tech, streaming giants, and telecom (Information) command massive market valuations and global headlines, yet they represent a lean employment pool of just 3.2 million workers (2.0% of the workforce).
* The Heavy Industry Baseline: Combined, Construction and Manufacturing still account for over 21 million physical on-site jobs in the US, remaining critical foundational pillars for blue-collar employment despite the dominant rise of white-collar and service-based industries.

##  The World

### 10-Year Change in Percentage Share of the Global Workforce [3]

    Prompt: Do the same Job Percentage analysis for the worldwide economy

When analyzing labor markets on a global scale, tracking 21 detailed industry codes is impossible due to varying regional infrastructure. The [International Labour Organization (ILO)](https://ilostat.ilo.org/) and the [World Bank](https://data.worldbank.org/indicator/SL.AGR.EMPL.ZS) bypass this by condensing the entire global workforce (estimated at ~3.4 billion workers) into three broad macroeconomic sectors: Services, Agriculture, and Industry. [1]
Over the last decade, the global workforce grew by roughly 300 million net jobs. The global data reveals a powerful structural transition: humanity is rapidly urbanizing, moving away from rural farm work and transitioning directly into the service economy. [2]

| Global Macro Sector [2, 4, 5] | broad Industry Sector Description | 2016 Global Job Share | 2026 Global Job Share | Percentage Point (pp) Shift | Approx. Global Workers Today |
|---|---|---|---|---|---|
| Services | Retail, Tech, Health, Transport, Tourism, Corporate & Public Sectors | 48.7% | 51.8% | +3.1 pp (Largest share gain) | ~1.76 billion |
| Agriculture | Farming, Commercial Forestry, Animal Husbandry & Fishing | 28.5% | 25.2% | -3.3 pp (Largest share loss) | ~0.86 billion |
| Industry | Manufacturing, Mining, Construction & Utilities | 22.8% | 23.0% | +0.2 pp | ~0.78 billion |

### Key Decadal Global Workforce Shifts

* The Services Era: Services officially employ more than half of all humanity (51.8%). This rapid +3.1 percentage point expansion is driven by mobile telecommunications, digital financial services, and localized urban commerce across developing economies in South Asia, Latin America, and Sub-Saharan Africa.
* The Flight from the Field: Agriculture shed a massive 3.3 percentage points of its worldwide labor share. Millions of workers left subsistence farming for city centers, catalyzed by automation, industrial farming techniques, and climate pressures. Despite this reduction, agriculture remains a massive pillar of human employment, holding a quarter of all global jobs—a stark contrast to the UK's minor 0.9% or the EU's 4.6%.
* The Industrial Equilibrium: The manufacturing, construction, and heavy industry block (Industry) remained remarkably stable, creeping up slightly by +0.2 percentage points. While advanced Western nations continue to de-industrialize, emerging industrial engines across Southeast Asia (such as Vietnam, India, and Indonesia) have absorbed those production ecosystems, balancing the global total. [1, 2, 5, 6]

### Structural Contrast: UK vs. EU vs. The World

| Sector Block | UK Share of Jobs | EU Share of Jobs | Global Share of Jobs |
|---|---|---|---|
| Services | ~85.0% | ~67.7% | 51.8% |
| Industry | ~14.1% | ~22.0% | 23.0% |
| Agriculture | ~0.9% | ~4.6% | 25.2% |

The macro breakdown illustrates a clear economic spectrum. The UK functions as a highly specialized, hyper-financialized service-dominant economy. The European Union retains a robust, dual-engine approach balanced between services and high-value industrial production. The global average highlights a developing economy blueprint, where one in four humans still works directly in the earth or oceans to sustain the global supply chain. [4, 7]

[1] [https://data.worldbank.org](https://data.worldbank.org/indicator/SL.IND.EMPL.ZS)
[2] [https://ourworldindata.org](https://ourworldindata.org/grapher/share-employment-agriculture-industry-services)
[3] [https://www.weforum.org](https://www.weforum.org/stories/2020/01/future-of-work/)
[4] [https://data.worldbank.org](https://data.worldbank.org/topic/agriculture-and-rural-development)
[5] [https://data.worldbank.org](https://data.worldbank.org/indicator/SL.IND.EMPL.ZS)
[6] [https://reports.weforum.org](https://reports.weforum.org/docs/WEF_Future_of_Jobs_Report_2025.pdf)
[7] [https://worldmapper.org](https://worldmapper.org/maps/agricultural-workers-2015/)
