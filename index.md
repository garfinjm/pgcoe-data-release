---
title: PGCoE Considerations for Public Release of Pathogen Data
layout: minimal
---


# Considerations for Public Release of Pathogen Genomic Data

**Purpose**

Public data sharing is a cornerstone of modern infectious disease genomic epidemiology. At the same time, it is critical to protect the health data of individuals and maintain the reputations of public health agencies as reliable sources of information. When onboarding a new sequencing project, agencies must determine which data should be openly shared and which should be withheld to balance the benefits and risks of open data sharing. The purpose of this document is to facilitate internal discussions around public release of pathogen genomic data in public health agencies.

**Usage**
Public health agencies should start by assuming all data will be made public and then apply mitigation strategies and/or withhold data as valid concerns with sharing are identified. This framing ensures that the richest possible data is shared with the public. For example, an agency would choose to withhold the specific birth date of a sampled individual (which they have determined to be too identifying to release) and instead supply the age of that individual (which is harder to trace back to one person).

**Why share data publicly?**

Analysis of pathogen genomic data to support surveillance and outbreak response benefits greatly from accessing publicly available sequence data. When an agency is able to contextualize their data with data collected from other jurisdictions, they are better able to understand how outbreaks originated, how infectious disease transmission might be connected across jurisdictions, and how what they’re seeing compares to other areas of the United States. Open data sharing by public health agencies ensures that they give back to the community and system that they benefit from.

There is no one-size-fits-all plan for sharing pathogen genomic data. The technical methods being used, pathogen being examined, geographic and demographic populations the pathogen infects, and severity of the outbreak all factor into risk-reward calculations when determining what data to release, when to release it, and the level of detail to include. For this reason, rather than providing a checklist of data to share, we have outlined five common concerns, particular ways those concerns manifest, and commonly accepted mitigation strategies (where applicable).

**Common Concerns**

1. Publicly released data could be used to identify an individual.
2. Loss of control around how data are used, analyzed, and communicated after public release.
3. Inaccurate or misleading data could be released.
4. Public data release may be restricted and/or required by existing contracts or agreements.
5. Public data sharing is technically difficult and/or resource intensive.

## Concern 1: Publicly released data could be used to identify an individual.

To protect individual privacy, data submitters must ensure that no information provided to public databases can lead to identification of a specific person. This includes removing directly identifying information (e.g. names) as well as metadata or genomic data that could enable identification through indirect means. Appropriate data handling depends on many factors, including pathogen characteristics, host population, sampling methods, sequencing techniques, and the data format intended for submission.

- **Organism and population characteristics can allow reidentification of an individual through sequence metadata:** In highly rare pathogens or sparsely populated geographic regions, data including collection date, facility, state, or age are more identifying than for common pathogens or densely populated areas. These sequence metadata should be considered carefully prior to sharing. It is important to remember that as metadata provided with sequencing data is reduced, the public health utility of the sequence data is also reduced. Some metadata (for example sample collection dates) are extremely important and should not be obscured or withheld without good reason.

> {: .mitigation } 
  > > Reduce detail of identifying metadata fields in cases where that data is likely to be identifying (ex. submit collection location to state level instead of county level for sparsely populated counties.)
  > >
  > > {: .cost }
  > > > This strategy reduces the resolution available for future investigations which can make some genomic epidemiology techniques less effective or impossible.
  > >
  > > {: .prevalence} 
  > > > Varies by metadata type, common for geographic information.
>
> {: .mitigation } 
  > > Withhold metadata fields in cases where that data is likely to be identifying and there is a **substantial** risk to the organization submitting the data or the individual the data was generated from. In these cases, best practice is to indicate that the data was collected but not shared publicly by using a term like “Not Given” or “Withheld”.
  > >
  > > {: .cost }
  > > > This strategy removes data fields available for future investigations which can make some genomic epidemiology techniques less effective or impossible.
  > >
  > > {: .prevalence} 
  > > > Common for some highly identifying metadata fields (ex. name). Generally, it is preferable to reduce detail (see above) rather than withhold data entirely.

- **Some sampling, sequencing, and data processing methods may capture human genetic data**: The type of sample that has been sequenced influences the data handling practices that are best suited to data submission. Laboratories should consider the extent to which the target organism is isolated or enriched relative to any human genetic material when designing their requirements for data processing and assessment prior to submission.
> {: .mitigation } 
  > > Use methods (like isolating or enriching for the target pathogen) which minimize off-target sequencing of human material.
  > >
  > > {: .cost }
  > > > These methods often introduce bias in what is sequenced and often do not completely eliminate human genomic data.
  > >
  > > {: .prevalence} 
  > > > Very common when sequencing directly from clinical specimens without an isolation step (ex. targeted tiled amplicon sequencing of a virus from a nasal swab).
> 
> {: .mitigation } 
  > > Apply in-silico dehosting software to data before public sharing.
  > >
  > > {: .cost }
  > > > Dehosting software is not perfect; it may leave small amounts of human genomic data and may remove small amounts of pathogen data from the dataset.
  > >
  > > {: .prevalence} 
  > > > Very common in methods (ex. untargeted genomic sequencing) which produce a large amount of human genomic bycatch. Not typically used when an organism is sequenced from culture.
> 
> {: .mitigation } 
  > > Share data types which are less likely to contain human data (ex. assemblies instead of raw reads or aligned reads instead of raw reads)
  > >
  > > {: .cost }
  > > > Limits some analytical approaches. May remove meaningful data if assembly is not high quality. This is a good choice if sharing reads is not an option.
  > >
  > > {: .prevalence} 
  > > > Required by some programs, generally the two strategies above are preferred.

## Concern 2: Loss of control around how data are used, analyzed, and communicated after public release.

The release of genomic data, and analysis by non-public health entities, can shape public perception of risk in an emerging situation, affect trust in health authorities, and impact the effectiveness of public health responses. Public health agencies must navigate the complexities of timely data sharing while ensuring that the information is properly contextualized and accurately communicated to prevent misinformation and inaccurate interpretations. Engaging with communications staff and establishing clear protocols for data release can help mitigate the risks associated with public narrative management. By strategically timing the release of genomic data and preparing for potential media inquiries, public health agencies can provide the most accurate information to the public and maintain confidence in public health initiatives, and therefore more effectively respond to public health threats.

- **Sequence data with meaningful ramifications for public health, released without accompanying public messaging, may give the appearance of an uncoordinated or unwary public health agency.** The most common example of this is a laboratory discovering a pathogen not previously identified within their agencies’ jurisdiction which could have an important public health impact.
> {: .mitigation } 
  > > Work with internal agency communications staff to create timely press releases to ensure that messaging is clear, accurate, and aligned with the public health goals of the agency.
  > >
  > > {: .cost }
  > > > Intra-agency communications can delay release of data.
  > >
  > > {: .prevalence} 
  > > > Extremely common for data releases that are likely to be newsworthy. Not as common for low impact or routine projects.
> 
> {: .mitigation } 
  > > Engage with external stakeholders (local health departments, policymakers, community leaders, etc.) early and often in discussions around data release. By providing these stakeholders with advance notice and context about the data, public health agencies can prepare them to address public inquiries and concerns effectively.
  > >
  > > {: .cost }
  > > > Few costs to early engagement with stakeholders.
  > >
  > > {: .prevalence} 
  > > > Varies by project and setting.
> 
> {: .mitigation } 
  > > Prepare and review data sharing and communication plans when collaborating with academic or private partners prior to public release of data. This collaborative review can help ensure the correct interpretation and the narrative around the findings of the investigation is well-crafted to reduce the risk of miscommunication.
  > >
  > > {: .cost }
  > > > Intra-agency communication can delay release of data.
  > >
  > > {: .prevalence} 
  > > > Varies by project and setting.
- **Sequence data released publicly without messaging may not be interpreted correctly.** During an infectious disease outbreak investigation, sequencing data is just one of the many types of laboratory and epidemiological data collected by a public health agency. It’s not unreasonable to expect that an external observer looking only at the publicly shared sequence data could unintentionally (or intentionally in the case of a bad actor) come to an incorrect conclusion.
> {: .mitigation } 
  > > Build internal genomic analysis capacity so that results and interpretation can be shared in tandem quickly after data generation. While rapid data release is a significant public service, communicating findings from analysis of those data is usually more useful and can build trust that information is being shared as it is learned.
  > >
  > > {: .cost }
  > > > Genomic analysis capacity personnel and infrastructure both carry substantial financial costs.
  > >
  > > {: .prevalence} 
  > > > Varies, well-resourced organizations are more likely to have existing staff with the necessary expertise.

- **Agencies sharing data in real-time risk being “scooped” on their publications by external groups analyzing data.** While this is a more common concern for academic laboratories, public health agencies may hesitate to release genomic data due to concerns that outside groups may analyze the data before the data generators and publish their findings without crediting and including data generators at the public health agency.
> {: .mitigation } 
  > > Use a resource like* [*Pathoplexus*](https://pathoplexus.org/) *for real-time data submission allowing the public to access the data with stricter usage conditions for a limited period until data is released more permissively on a resource like NCBI.
  > >
  > > {: .cost }
  > > > Setup time for a new submission pathway.
  > >
  > > {: .prevalence} 
  > > > Somewhat common, though not preferred compared to submitting to a more open repository.

## Concern 3: Inaccurate or misleading data could be released.

Ensuring confidence in data is essential for maintaining trust, supporting sound decision-making, and enabling timely public health and scientific action. Confidence is achieved through deliberate quality assurance (QA) practices that balance accuracy, completeness, and transparency against the urgency of data release. Institutions must navigate trade-offs between rapid dissemination and rigorous validation, particularly in contexts involving emergent threats, limited reference materials, or high-impact outcomes.

While the best practice is to release data as soon as possible after sequencing, delays in data release may be justified when additional scrutiny is required to meet quality standards aligned with the intended use of the data. These delays can be reduced by establishing clear standards, protocols, and validated workflows for common or anticipated data types in advance. Formal QA validation—often requiring empirical measures of precision and accuracy—is frequently mandated prior to release, but familiarity with institutional quality management systems and proactive workflow validation can significantly streamline this process.

- **Data released without sufficient QA could be incorrect.** Inaccurate or incomplete data can lead the public or organizations to make inaccurate conclusions or poor decisions. Before release all data should be certified as adhering to internal quality standards and protocols. In some cases, this could delay the release of data. Depending on the magnitude of the public health impact caused by sharing data, it may be appropriate to deviate from standard protocols after discussion with quality personnel.
> {: .mitigation } 
  > > Ensure staff are trained and familiar with QA standards so they can respond to emergency situations efficiently.
  > >
  > > {: .cost }
  > > > Training time for staff to learn and maintain familiarity with QA standards.
  > >
  > > {: .prevalence} 
  > > > Very common in labs performing laboratory developed tests. It is also generally good practice to build and maintain an understanding of QA standards and principles among staff developing or implementing new tests.
> 
> {: .mitigation } 
  > > Ensure that agency QA standards are well documented so that staff can be trained on those standards.
  > >
  > > {: .cost }
  > > > Time to develop and formalize QA standards.
  > >
  > > {: .prevalence} 
  > > > Standard practice in regulated environments.

- **Established QA standards cannot be met due to lack of reference materials**. Timely assessment of data quality can be challenging when there are limited or no standard reference materials that can be used for comparison. This is often the case when attempting to release data from a rare, emergent, or novel disease.
> {: .mitigation } 
  > > Compare the results from multiple independent methods performed internally or by one or more external institutions (e.g., confirmation testing by CDC).
  > >
  > > {: .cost }
  > > > Time to identify and implement orthogonal methods or coordinate with external institutions.
  > >
  > > {: .prevalence} 
  > > > Very common during development in the absence of reference material.
- **Perceived data quality could change as new data emerges.** In developing situations, the perceived quality of data may change as new information becomes available.
> 
> {: .mitigation } 
  > > Ongoing communication with stakeholders is critical not only for newly generated data, but also for previously communicated data and findings.
  > >
  > > {: .cost }
  > > > Minimal when ongoing communication is happening anyway.
  > >
  > > {: .prevalence} 
  > > > Common.
> 
> {: .mitigation } 
  > > Be prepared to update publicly shared data and have a plan to announce any updates to stakeholders.
  > >
  > > {: .cost }
  > > > Time to prepare new messaging and to update data.
  > >
  > > {: .prevalence} 
  > > > Common.

## Concern 4: Public data release may be restricted and/or required by existing contracts or agreements.

In addition to institutional factors that must be considered before public data release, there are typically extra-institutional factors to consider as well. Before a new type of data is released publicly, it is important to consider any restrictions on data sharing that may be imposed by laws or legal agreements with other institutions (including funding agencies). Conversely, data sharing might be required by outside institutions, funding agencies, and peer-reviewed journals. Public health agencies should be aware of all these external factors that can shape data sharing and release.

- **Funding agencies may require release of data**. Different jurisdictions and funding bodies may have varying requirements for what data can or must be publicly shared.
 > {: .mitigation } 
  > > When applying for funding, make sure the data sharing requirements are compatible with your agency policies, goals, and mission.
  > >
  > > {: .cost }
  > > > None.
  > >
  > > {: .prevalence} 
  > > > Common.

- **Data generated under Institutional Review Board (IRB) oversight or covered by Health Insurance Portability and Accountability Act (HIPAA) have limitations on public data sharing.** Large swaths of work done in public health agencies are exempt from IRB and HIPAA oversight. However, organizations or activities covered by IRB or HIPAA are subject to additional restrictions on data sharing. IRB provisions must be made to address the use of residual specimens for additional studies and management of any clinically relevant results identified by research testing. These regulations typically have specific rules about the kinds and resolution of data that can be shared depending on the conditions under which they are released.
- **Uncertainty about releasing sequence data from Select Agent organisms.** The Federal Select Agent Program does not (as of mid-2026) regulate digital representations of nucleic acid sequences and select agent sequences can be shared publicly. However, would-be submitters should carefully consider whether sharing select agent sequencing data may impact potential criminal investigations, as in cases of bioterrorism. Comprehensive information on the Federal Select Agent Program is available at [selectagents.gov](https://aphl8515.sharepoint.com/sites/PGCOERBSC2/Shared%20Documents/General/selectagents.gov).
- **Journals require data to be shared for publication.** Reporting findings in scientific journals requires public release of genomic data and a minimal set of associated metadata, while generally redacting data that are not necessary for the following purposes:
  - **Reproducibility of analyses:** Any important inferences, findings or conclusions should be reproducible by a reader or reviewer from publicly released data and described methodology, without having to request further information or contact the authors. In an ideal world, this includes the ability for a reader to reproduce genome assemblies from published sequence reads and described informatic methods. More importantly is the ability for a reader to reproduce any phylogenies, statistical correlations, and other inferences from released metadata and genomic data.
  - **Data reusability:** Pathogen genomic data and metadata should be released with enough information such that it becomes a useful addition to future analyses and inferences performed by other groups, without having to request further information from the authors.

## Concern 5: Public data sharing is technically difficult and/or resource intensive.

Outside of the legal, logistical, and institutional barriers that might hinder an organization from submitting data to a public repository, there can also be technical and logistical barriers to completing the steps required for data sharing. To properly release data, an organization must know what resource they want to use to share data, how data is organized on that resource, and how to format their existing data to be compatible with the resource. Additionally, there can be a learning curve for new users when beginning to sort, filter, and wrangle data into a format which is acceptable for submission to a public repository, and they may not be aware of existing tools and resources to help with that challenge.

PGCOE Response Base Working Group has created [a website to address the most common technical hurdles](https://Update.this.url.eventually) to sharing sequencing data publicly on NCBI. Organizations are strongly encouraged to use this resource in addition to NCBI’s first party documentation to address technical hurdles encountered during data submission.

- **Staff are not familiar with data submission process.** Public data sharing repositories like [NCBI](https://www.ncbi.nlm.nih.gov/) and [Pathoplexus](https://pathoplexus.org/) manage users and store data in structures that are not necessarily intuitive to new users. This often slows adoption of these resources by new submitters.
> {: .mitigation } 
  > > Ensure staff are trained and familiar with repositories’ structure and upload procedure so they can respond to emergency situations effectively.
  > >
  > > {: .cost }
  > > > Time to train and maintain competency of staff.
  > >
  > > {: .prevalence} 
  > > > Very rare.
> 
> {: .mitigation } 
  > > Utilize existing tools to make data upload easier (ex.* [*SeqSender*](https://github.com/CDCgov/seqsender)*,* [*TOSTADAS*](https://github.com/CDCgov/tostadas)*, etc.)
  > >
  > > {: .cost }
  > > > Upfront cost in time to learn and implement another piece of software (this is offset over time).
  > >
  > > {: .prevalence} 
  > > > Common in settings where routine or high-volume uploads are required.

- **Formatting sequence metadata for upload is labor intensive.** Public data sharing repositories require that sequence metadata be formatted and stored in specific ways to facilitate smooth data transfers. Organizing, formatting, and transforming the required data is labor intensive, but essential to making uploaded data useful.
> {: .mitigation } 
  > > Develop flexible internal tooling and scripts to convert sequence metadata to be compatible with submission processes.
  > >
  > > {: .cost }
  > > > Often considerable development time to create scripts and training time to teach staff how to use those scripts.
  > >
  > > {: .prevalence} 
  > > > Very common for frequent data submitters, less common in agencies with lower throughput.
> 
> {: .mitigation } 
  > > Foster consistency in how data is stored and formatted within the organization.
  > >
  > > {: .cost }
  > > > Time spent convincing staff that consistency is worthwhile. Infrastructure costs for more complex data storage systems.
  > >
  > > {: .prevalence} 
  > > > Varies.

## Conclusion

Public data sharing is increasingly important to ensure accurate and actionable genomic epidemiology. All data sharing and communication by public health agencies carries some level of risk. When sharing pathogen genomic data, agencies must balance individual privacy and institutional reputation with the immense public health value of an open, global pathogen genomic data pool. By adopting a “default-to-open” genomic data sharing policy and thoughtfully applying risk mitigation strategies (with the understanding that some strategies drastically reduce the utility of shared data) public health agencies can maximize the benefits of their data while safeguarding against potential risks.

When planning a new sequencing project, public health agencies should take time early in implementation to consider not only what and how pathogen genomic data will be shared with the public, but also what groups exist outside and within their agency that may have a stake in any findings from the project. Internally, this means engaging with communications teams. Externally, national/state/local/tribal public health agencies and medical systems are critical stakeholders for new surveillance projects.

Implementing the procedural and technical systems required for efficient, risk-aware data sharing demands an investment of time and resources with returns that are not always immediately tangible. However, as public health agencies commit to open data sharing, the resulting public datasets become invaluable. Over time, this pool of public data not only enhances core agency goals like pathogen surveillance and outbreak response, but also boosts basic scientific research, accelerates drug and vaccine development, and informs future public health policy.


