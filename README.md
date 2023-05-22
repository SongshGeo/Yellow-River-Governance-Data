# Dataset description

[![DOI](https://zenodo.org/badge/643696180.svg)](https://zenodo.org/badge/latestdoi/643696180)

**version**: v-1.1.0

This repo storages datasets for the research **"Identifying regime transitions for water governance at the Yellow River Basin (YRB), China"**, submitted to *Water Resources Research* (WRR).

| Dataset | Sheets | Time span | Description |
|---------|----------------|-----------|-------------|
| **Reservoirs** | reservoirs.csv | 1956-2021 | Dataset of significant new reservoirs built in the YRB since 1956, including major reservoirs constructed mainly for regulating and managing. |
| **Measured Runoff** | runoff.csv | 1956-2021 | Annual measured runoff data collected from the Yellow River Sediment Bulletin and four controlling stations measuring different reaches of the Yellow River. |
| **NLWUD water uses** | perfectures_YR_WU.csv | 1965-2013 | Water use dataset from the National Long-term Water Use Dataset of China (NLWUD), including water uses, water-consuming economic variables, and water use intensities by sectors at the prefecture level. |
| **Bulletin water uses** | groundwater_WU.csv, runoff_WU.csv | 2001-2021 | Water use dataset from Yellow River Water Resource Bulletins. |
| **Laws** | crucial_laws.xlsx | 1949-2013 | Important laws related to the Yellow River at the basin scale from the last century. |
| **Big Events Records** | big_events.csv | 1949-2015 | Original "big events" documents related to the Yellow River governance from the Yellow River Water Conservancy Commission (YRCC), the agency at the basin scale. |

## Reservoirs

Dataset of significant new reservoirs built in the YRB since 1956.
Among all the reservoirs, YRCC [labelled the ``major reservoirs''](http://www.yrcc.gov.cn/hhyl/sngc/) which were constructed mainly for regulating and managing.

**Fields**:

- Year [Numeric]: time when the reservoir was built.
- capacity [Numeric]: water storage capacity.
- name [String]: name of the reservoir.
- province [String]: which province belongs to.
- region [Cate]: which region this reservoir belongs to. Source Region (SR), Upper Region (UR), Middle Region (MR), or Lower Region (LR).
- major [Bool]: If this reservoir is major reservoir (crucial role for basinal regulating, 1) or not (0)

## Measured Runoff

Annual measured runoff data was collected from the [Yellow River Sediment Bulletin](http://www.yrcc.gov.cn/nishagonggao/), originally. Four controlling stations are measuring different reaches of the Yellow River:

- **Tangnai Hai**: controlling station of the Source Region (SR) within the YRB.
- **Toudao Guai**: controlling station of the Upper Region (UR) within the YRB.
- **Huayuan Kou**: controlling station of the Middle Region (MR) within the YRB.
- **Lijin**: controlling station of the Lower Region (LR) within the YRB.

Their locations are:

| Station     | Longitude   | Latitude    |
| ----------- | ----------- | ----------- |
| **Tangnai Hai** | 100.148527  | 35.516798   |
| **Toudao Guai** | 111.188     | 40.224617   |
| **Huayuan Kou** | 113.671166  | 34.904219   |
| **Lijin**       | 118.296685  | 37.501814   |

## NLWUD Water uses

Water use dataset filtered from the National Long-term Water Use Dataset of China (NLWUD). Original dataset can be found at [Figure Share](https://figshare.com/articles/dataset/Zhou_et_al_2020_PNAS_dataset_xlsx/11545176), detailed information can be found at Zhou et. al., (2020):

- [Zhou, F.; Bo, Y.; Ciais, P.; Dumas, P.; Tang, Q.; Wang, X.; et al., Deceleration of China’s human water use and its key drivers. PNAS. 2020, 117: 1-10.](https://doi.org/10.1073/pnas.1909902117).

We determined the prefectures belong to the YRB by filtering the NLWUD dataset with a threshold of $95\%$ intersected area. Filtered dataset can be found in `prefectures_YR_WU.csv`

## Bulletin water uses

Water use dataset from [Yellow River Water Resource Bulletins](http://www.yrcc.gov.cn/zwzc/gzgb/gb/szygb/). Two sheets (groundwater_WU.csv and runoff_WU.csv) store statistical water uses data from groundwater and surface water, separately. Data was reported by province annually with two items (withdraw and consumption) and six sectors (Irrigation, Livestock, Industry, Cities, Domestic, Ecological).

**Fields**:

- Year [Numeric]
- Province [String] provinces' name.
- Item [Cate]: water consumption or water withdraw.
- Total [Numeric]: total water use.
- Irrigation [Numeric]: water used on irrigating.
- Livestock [Numeric]: water used on forest grazing, fishing and livestock.
- Industry [Numeric]: water used on industrial productions.
- Cities [Numeric]: Urban service industry.
- Domestic [Numeric]: Domestic water use.
- Ecological [Numeric]: Water uses on ecological restoration.

## Laws

Important laws related to the Yellow River at the basin scale from the last century. These crucial laws are stressed in "Yellow River Basin Comprehensive Plan (2013)".

- [Yellow River Water Conservancy Commission (2010) Yellow River Basin Comprehensive Plan. Zhengzhou, Henan: Yellow River Water Conservancy Press]((https://www.amazon.com/Yellow-River-Comprehensive-2012-2030-Chinese/dp/7550906580/ref=sr_1_1?keywords=9787550906587&linkCode=qs&qid=1684724739&s=books&sr=1-1)). (Accessed: 3 February 2023).

**Fields**:

- name [String]: Chinese name of the law.
- year [Numeric]: implementation or revision time of the law.
- agency_ch [String]: Chinese name of the implementation agency.
- agency_en [String]: English name of the implementation agency.

## Big Events Records

Original "big events" documents related to the Yellow River governance from the Yellow River Water Conservancy Commission (YRCC), the agency at the basin scale. The data was crawled from [YRCC's official website](http://www.yrcc.gov.cn/hhyl/hhjs/zhrmghg/).

**Fields**:

- id [String]: Original ID of the item on the website.
- Title [String]: brief summary of the event.
- Year [Numeric]: Which year did the event happen.
- Month [Numeric]: Which month did the event happen.
- Text [String]: detailed description of the event.

## IWGI

Calculation results of Integrated Water Governance Index (IWGI). Combining three indicators: water stress (IS), water using purposes (IP), and water allocation (IA). Details can be found in the paper submitted to *Water Resources Research*.

## License

Creative Commons Attribution 4.0 International

Data may be freely downloaded for research, study, or teaching, but must be cited appropriately. Re-release of the data, or incorporation of the data into a commercial product, is allowed only with explicit permission. If you would like to request permission to use this dataset for another purpose, please contact us at [shuaiwang@bnu.edu.cn](mailto:shuaiwang@bnu.edu.cn)

## Funding

Funding was provided by the National Natural Science Foundation of China (CN) (Grant Nos. NSFC 42041007).
