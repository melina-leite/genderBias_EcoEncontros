# README and METADATA

Original study published as Preprint in EcoEvoRxiv **"Is the audience gender-blind? Smaller audience in female talks highlights prestige differences in academia"** (https://doi.org/10.32942/X25607). Submitted for recommendation to Peer Community in Ecology.

The present repository contains data, metadata, and modeling analysis source codes necessary to reproduce the EcoEncontros gender bias results. The EcoEncontros is a seminar series of weekly talks at the Ecology Graduate Program at the University of São Paulo (PPGE, IB-USP). The information from all talks between 2008 and 2019 from the EcoEncontros committee attendance list archives (N=344 talks) are presented. We retrieved data about the speaker (gender, academic level, and affiliation) and the seminar (date, title, abstract, and audience size). We inferred the speaker's gender by name and photo (always present on the seminars’ posters). We have removed the speakers' names from the data files provided in order to maintain their anonymity.

## The content is organized into four sections, each with one specific aim:

-   `0_data_summary`: data description, wrangling, and summary statistics. It starts with raw presentation data from 2008 to 2019 (data folder; see metadata below).

-   `1_speakers_genderPosition`: modeling source code of objective 1 analyses on gender bias in speakers and academic level.
    Here, we assess the proportions of female speakers by academic level, before and after affirmative actions.
    We do an extra analysis with only the speakers belonging to the PPGE community, to evaluate if the proportion of female speakers is proportional to the proportion of female academics in the PPGE community.

-  ` 2_audience_genderPosition`: modeling source code of *objective 2* analyses on gender bias in *audience size* of seminars and academic level.
    Here, the audience size (\# number of attendants in the seminar) is modeled by the gender (male, female), the academic level (student, postdoc, professor) of the speaker, and affirmative actions (before and after).

-   `3_text_genderAnalysis`: modeling source code of *objective 3* containing text analysis from titles and abstracts of the talks.

When using this data, please cite the Zenodo permanent version of this repository:

> Leite, Melina de Souza & Rodrigues Barreto, Júlia (2024). Data and Code from: Is the audience gender-blind? Smaller audience in female talks highlights prestige differences in academia (v0.9.9). Zenodo. https://doi.org/10.5281/zenodo.11288110. 

## Metadata of the raw data file "presentations_PPGE_2008-2019.csv"

Variables:

* id = Unique label of presentation ordered in date.
* date = date of presentation in "DD-MM-YYYY" format.
* code_speaker = speaker identification code.  
* gender = binary gender of the speaker (Female or Male). We are aware that this binary classification caveat may not reflect the self-declaration of gender.  
* title_original = original title of the talk (in original language).  
* title_language = original language of the talk title.  
* title_english = talk title in English. Whenever not originally given in English, it is translated by the authors and validated using DeepL software.  
* abstract_original = original abstract (in original language).  
* abstract_language = original language of the talk abstract.  
* abstract_english = talk abstract in English.  
* audience_n = \# number of attendees.  
* audience_female = \# number of female attendees.  
* audience_male = \# number of male attendees.  
* audience_NA = \# number of attendees without F/M gender identification.  
* department = institutional department of affiliation origin.  
* institute = institute of affiliation origin.  
* university = university or institution of affiliation origin.  
* country = country of affiliation's university or institution of origin.  
* position = speaker's academic level.  
* position_cat = speakers academic level category classified into 3 categories: student (bachelor’s, master’s, or doctoral degrees), postdoctoral researcher, and professor.  
* origin = code or origin of the speaker: home institution of the seminar series (IB, Institute of Biosciences in the University of São Paulo), Brasil, Latin America ("AmLat"), North America ("AmNorte"), Europe ("Europa") or Australasia.  
* total_citation_n = \# Number of professor speaker citations from respective Google Scholar profiles.  
Source: <https://scholar.google.com>, accessed in 2021.  
* h_index = \# Number of publications for which the professor speaker has been cited at least that same number of times, collected from its respective Google Scholar profile.  
* i10_index = \# Number of professor speaker's papers with at least 10 citations, collected from its respective Google Scholar profile.  
* most_cited_n = \# Number of citations of the most cited paper, collected from the professor speaker's Google Scholar profile.  
* citation_cum = cumulative \# number of citations until the year of the talk.  
* years_career = professor speaker's career length, measured as the number of years from the first cited publication until the year of the talk.  
* nature_index_count = Count Nature index, where a count of one is to an institution or country if one or more authors of the research article are from that institution or country, regardless of how many co-authors there are from outside that institution or country.  
Source: <https://www.nature.com/nature-index/>, accessed in 2021.  
* nature_index_share = Share Nature index, a fractional count that considers the percentage of authors from that institution and the number of affiliated institutions per article (Nature Index, 2021).  
* obs = any necessary information regarding specific talk.  

We also collected information on the gender balance for each academic level in the Graduate Ecology Program during the same period (2008-2019), which is in the file "pop_PPGE_2008-2019.csv" within the data folder and explained in the Rmd script `0_data_summary`.

## Owners:

[Melina Leite](https://melinaleite.weebly.com/) e [Júlia Barreto](barretoj@usp.br)
