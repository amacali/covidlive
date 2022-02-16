# COVID Live Data on COVID-19 (coronavirus) for Australia #
### 🗂️ Download our COVID-19 dataset: ###
- **CSV:** [https://covidlive.com.au/covid-live.csv](https://covidlive.com.au/covid-live.csv)
- **JSON:** [https://covidlive.com.au/covid-live.json](https://covidlive.com.au/covid-live.json)

Our complete dataset is a collection of COVID-19 maintained by *[COVID Live](https://covidlive.com.au/about)*. COVID Live data is collected from media releases and [verified](https://covidlive.com.au/last-updated) against state and federal health departments.

## Dataset ##
Our COVID-19 dataset is available in [CSV](https://covidlive.com.au/covid-live.csv) and [JSON](https://covidlive.com.au/covid-live.json) formats and includes all historic data.

### 📅 Reporting Window ##
| Field | Description |
| --- | --- |
| `REPORT_DATE` | Reporting date AEDT |
| `LAST_UPDATED_DATE` | Time of last update |
| `CODE` | State or territory code. AUS for Australia |
| `PREV_%` | Value of previous reporting date |

### 🦠 Confirmed Cases ##
| Field | Description |
| --- | --- |
| `CASE_CNT` | Total confirmed cases for COVID-19 |
| `NEW_CASE_CNT` | New cases in the last 24 hours |
| `PROB_CASE_CNT` | Total confirmed rapid antigen test cases for COVID-19. Included in `CASE_CNT` total |
| `TEST_CNT` | Total tests for COVID-19 |
| `DEATH_CNT` | Total deaths attributed to COVID-19 |
| `ACTIVE_CNT` | Total active cases for COVID-19 |
| `RECOV_CNT` | Total recoveries for COVID-19 |
| `MED_HOSP_CNT` | Number of current cases admitted to hospital |
| `MED_ICU_CNT` | Number of current cases admitted to ICU |
| `MED_VENT_CNT` | Number of current cases requiring ventilation |

### ✈️ Source of Infection ###  
The total number of confirmed cases where:

| Field | Description |
| --- | --- |
| `SRC_OVERSEAS_CNT` | The person was infected while overseas |
| `SRC_INTERSTATE_CNT` | The person was infected in Australia, but not in the reporting jurisdiction |
| `SRC_CONTACT_CNT` | The person was infected in Australia through contact with someone confirmed to have COVID-19 |
| `SRC_UNKNOWN_CNT` | The person was infected in Australia, but the source of infection is not known |
| `SRC_INVES_CNT` | The source of infection has not yet been determined, but is currently being investigated through public health actions |

### 💉 Vaccinations ###
Vaccination data is sourced from the [Australian Government Department of Health](https://www.health.gov.au/resources/collections/covid-19-vaccination-daily-rollout-update) via [Ken Tsang](https://github.com/jxeeno/aust-govt-covid19-vaccine-pdf).

| Field | Description |
| --- | --- |
| `VACC_FIRST_DOSE_CNT` | Total number of people who received one dose |
| `VACC_FIRST_DOSE_CNT_12_15` | Total number of 12-15 year olds who received one dose |
| `VACC_FIRST_DOSE_CNT_5_11` | Total number of 5-11 year olds who received one dose |
| `VACC_PEOPLE_CNT` | Total number of people who received two doses |
| `VACC_PEOPLE_CNT_12_15` | Total number of 12-15-year olds who received two doses |
| `VACC_BOOSTER_CNT` | Total number of people who received more than two doses |

**Vaccinations by Provider location** is sourced from the Australian Immunisation Register and self reported data. It includes a breakdown of doses administered by State and Territory clinics (Hubs), Aged Care and Disability Facilities, and Primary Care (GPs).  

| Field | Description |
| --- | --- |
| `VACC_DOSE_CNT` | Total doses administered by location of provider |
| `VACC_AGED_CARE_CNT` | Total Commonwealth aged care and disability doses administered |
| `VACC_GP_CNT` | Total Commonwealth primary care and GP doses administered |
| `VACC_DIST_CNT` | Total number of doses distributed. |

**Vaccinations by State or Territory** of residence is also sourced from the Australian Immunisation Register. The National population will not equal the sum of listed jurisdictions due to a small number of people residing in some 'other' territories. First and Second dose breakdowns are only available by residence.


## Changelog ##
- **17 Feb 22** updated `CASE_CNT` for VIC and QLD to state health department figures (backdated to 8 Jan 21)
- **31 Jan 22** updated `CASE_CNT` for NSW and SA to state health department figures (backdated to 13 Jan 21)
- **28 Jan 22** added `NEW_PROB_CASE_CNT` and reconciled totals for ACT and NSW
- **13 Jan 22** added `VACC_FIRST_DOSE_CNT_5_11` and `VACC_FIRST_DOSE_CNT_5_11`
- **9 Jan 22** updated `MED_HOSP_CNT` for NT to territory health department figures (backdated to 20 Dec 21)
- **8 Jan 22** added `PROB_CASE_CNT` for self-reported rapid antigen test results
- **2 Jan 22** updated `RECOV_CNT` for NSW to standard formula (backdated to 1 Nov 21)
- **22 Nov 21** added `VACC_BOOSTER_CNT` for Australia
- **25 Oct 21** added `VACC_FIRST_DOSE_CNT_12_15` and `VACC_PEOPLE_CNT_12_15` to enable 12+ projections
- **4 July 20** a total of 189 historic `CASE_CNT` reported in crew members on board the Ruby Princess have been reclassified as Australian cases and are now included in NSW totals reported by the Commonwealth Department of Health.


## License ##
All data produced by COVID Live is available under the [Creative Commons BY license](https://creativecommons.org/licenses/by/4.0/).
