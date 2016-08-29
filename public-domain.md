# Liberating public domain science from paywalls

## Goal

Scientific articles that are in the public domain due to expired copyright or being un-copyrightable are currently being paywalled. This is not illegal, but it certainly is regretful. It means that the public domain versions are one of 3 things:

1. A freely available version of the public domain work is not readily findable

2. A freely available version of the public domain work is not readily findable because it does not exist (nobody has ever taken the effort to make one available)

3. A freely available version of the public domain work is not available because copyright is being wrongly asserted (sometimes called copyfraud)

### Determine what works are in the public domain 

#### Legal

 - [ ] Is the copyright term based on the author or the entity (i.e., publisher) when all copyright is transferred in a license agreement?
 - [ ] If based on the author, do *all* authors need to be deceased (i.e., the collective) and then 70Y PM (the longest)?
 - [ ] When exactly does something go into public domain? Based on copyright law at the moment of (1) publication or (2) at the moment it goes into PD?
 - [x] Can works be in the PD and then go back into copyright? E.g., 70Y postmortem, goes into PD, but in the next 10Y the laws change to 80Y postmortem. **Seems like they can, especially when laws are explicitly retroactive**
 - [ ] Which copyright legislation determines PD if publishers retain all copyright?
 - [ ] How long does copyright last for non-flesh copyright holders (e.g., pubs)? I think 100/120y but need to know for sure.
 - [ ] How does digitisation of works affect the copyright duration? (see [here](http://outofcopyright.eu/rights-after-digitisation/) as well)
 - [ ] Is federal funding sufficient to make US based works in the PD or is it only for federal *employees*? (see also [here](http://www.michaeleisen.org/blog/?p=1918))

 #### Architecture

 - [ ] Create local copy of the [CrossRef](https://crossref.org) database (WIP)
 - [ ] Create a daily update of the [CrossRef](https://crossref.org) database (WIP)
 - [ ] Determine public domain availability (e.g., [OutOfCopyright.eu](http://outofcopyright.eu/tools/); research in progress). *Might not be so easy after all, many fineprint legal issues. [Additional resources](https://archive.org/details/public_domain_calculators)*
 - [ ] Create a database with all unique author names, publication years, occurrences
 - [ ] `DupPD`: Identify potentially duplicate authors that are regarded as separate (based on name similarity, occurence in approximately same timeframe)
 - [ ] `RankPD`: algorithm to rank what authors are most important to be checked whether deceased based on number of publications, timeframe of publications (i.e., likelihood of public domain), and cross-referencing with `DupPD`
 - [ ] `CheckWD`: check whether authors are in WikiData and retrieve decease date (if available; [API](https://www.wikidata.org/w/api.php))

### Make these works available in an open repository

 - [ ] Collect the works that are in the public domain (e.g., with [ContentMine](https://github.com/contentmine) software)
 - [ ] Clean all metadata from these works (e.g., with the [Metadata Anonymization Tool](https://github.com/jvoisin/MAT/commits/master))
 - [ ] Create API interface with [Zenodo](https://zenodo.org) that uploads the work with the appropriate metadata from the CrossRef local store
 - [ ] Make sure the local store of CrossRef is updated to link to the Zenodo deposit (if successful)
