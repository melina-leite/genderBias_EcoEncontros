---
editor_options: 
  markdown: 
    wrap: sentence
---

# READ ME and METADATA

The present repository contains data, metadata and modelling analysis source codes necessary to reproduce the EcoEncontros gender bias results. The EcoEncontros is a seminar series of weekly talks at the Ecology Graduate Program at the University of São Paulo (PPGE, IB-USP). The information from all talks between 2008 and 2019 from the EcoEncontros committee attendance list archives (N=344 talks). We retrieved data about the speaker (gender, academic level , and affiliation) and the seminar (date, title, abstract, and audience). We inferred the speaker's gender by name and photo (always present on the seminars’ posters).

## The content is organized in four sections, each with one specific aim:

-   0_data_summary: data description, wrangling and summary statistics, that starts with raw presentations data from 2008 to 2019 (data folder, see metadata below).

-   1_speakers_genderPosition: modelling source code of objective 1 analyses on gender bias in speakers and career level.
    Here we assess the proportions of female speakers by academic level, before and after affirmative actions.
    Controlling for population proportions: the ratio of females at the graduate program by academic level and year.

-   2_audience_genderPosition: modelling source code of *objective 2* analyses on gender bias in *audience* of seminars and career level.
    Here the audience (\# number of attendants in the seminar) is modeled by the gender (male, female), the academic level (student, postdoc, professor) of the speaker, and affirmative actions (before, after).

-   3_text_genderAnalysis: modelling source code of *objective 3* containing text analysis from titles and abstracts.

When using this data, please cite: \* citation here\* ------

## Metadata of raw data file "presentations_PPGE_2008-2019.csv", variables:

id = Unique label of presentation ordered in date.
date = date of presentation in "DD-MM-YYYY" format.
code_speaker = speaker identification code.
gender = binary gender of the speaker (Female or Male).
We are aware that this binary classification caveat may not reflect the self-declaration gender.
title_original = original title of the talk (in original language).
title_language = original language of the talk title.
title_english = talk title in english.
Whenever not originally given in english, translated by the authors and validated using DeepL sorfware.
abstract_original = original abstract (in original language).
abstract_language = original language of the talk abstract.
abstract_english = talk abstract in english.
audience_n = \# number of audience attendees.
audience_female = \# number of female audience attendees.
audience_male = \# number of male audience attendees.
audience_NA = \# number audience attendees of unidentified binary gender.
department = institutional department of affiliation origin.
institute = institute of affiliation origin.
university = university or institution of affiliation origin.
country = country of affiliation's university or institution of origin.
position = speakers academic level.
position_cat = speakers academic level category classified into 3 categories: student (bachelor’s, master’s, or doctoral degrees), postdoctoral researcher, and professor.
origin = code or origin of speaker: home institution of the seminar series (IB,Institute of Biosciences in the University of São Paulo), Brasil, Latin America ("AmLat"), North Ametrica ("AmNorte"), Europe ("Europa") or Autralasia.
total_citation_n = \# Number of professor speaker citations from respective Google Scholar profile.
Source: <https://scholar.google.com>, accessed in 2021.
h_index = \# Number of publications for which the professor speaker has been cited at least that same number of times, collected from its respective Google Scholar profile.
i10_index = \# Number of of professor speaker's papers with at least 10 citations, collected from its respective Google Scholar profile.
most_cited_n = \# Number of citations of the most cited paper, collected from the professor speaker's Google Scholar profile.
citation_cum = cumulative \# number of citations until the year of the talk.
years_career = professor speaker's career length, measured as the number of years from the first cited publication until the year of the talk.
nature_index_count = Count Nature index, where a count of one is to an institution or country if one or more authors of the research article are from that institution or country, regardless of how many co-authors there are from outside that institution or country.
Source: <https://www.nature.com/nature-index/>, accessed in 2021.
nature_index_share = Share Nature index, a fractional count that considers the percentage of authors from that institution and the number of affiliated institutions per article (Nature Index, 2021).
obs = any necessary information regarding specific talk.

We also collected information on the gender balance for each academic level in the Graduate Ecology Program during the same period (2008-2019), contained in the file "pop_PPGE_2008-2019.csv" within data folder.

## Owners:

[Melina Leite](https://melinaleite.weebly.com/) e [Júlia Barreto](barretoj@usp.br)