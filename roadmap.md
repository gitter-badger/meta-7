# Roadmap

## Liberator

### Project Mission & Summary

Public access to the public domain is crucial, but not a given. A public park is public domain, but it can be subject to access restrictions (for example, not after dark). With information, it makes no sense to us that access needs to be restricted, because copying costs virtually nothing and has much potential. 

So why is this a problem? Example: this [research paper from 1871](http://dx.doi.org/10.1016/B978-0-08-006821-3.50008-8) can be freely available and reused, but isn't. Why? Because no one has made it available. This is just one of the 595,735 that are easy to identify as public domain of which public access isn't sure.

By ensuring public access to the public domain, we aim to build a decentralized resource for and with scholars, in order to facilitate radical innovation in consuming and contributing to scholarly information.


### Milestones
<!-- Pick 1-3 milestones. Depending on your project, milestones can vary: they may be related to software development goals, learning resources you’ll create, events or meetings you plan to hold, campaigns you’ll run. -->
<!-- List tasks to complete for each milestone. Write a short description of each task required to successfully complete project work on a milestone. Depending on your project, these might be items like: “Research existing Javascript learning resources for kids” or “Publicize the October Online Privacy Meet-up” or “Implement a new visualization scheme for the user-facing badges.” Be sure to time here to explain why you are doing this task. This will reinforce your vision for the project and help others see why each step is meaningful in the larger timeline. -->

1. Create an organized local copy of public domain works from CrossRef
	- [ ] Create a script to download CrossRef data based on filter
	- [ ] Create a script that structures raw json into PREFIX/DOI/crossref.json

2. Zenodo deposit procedure (Python based; ready to be implemented into Flask/Django)
	- [ ] Create a script that moves through crossref.json into a zenodo-deposit.json
	- [ ] Python script that deposits to Zenodo (with test function to operate in sandbox)

3. Metadata database
	- [ ] Create a PostgreSQL database
	- [ ] TABLE metadata (doi, deposited, )
	- [ ] TABLE zenodo (dois from zenodo)

4. Upload procedure (malware check, metadata writing to PostgreSQL)
	- [ ] Find which tools can be used to check the pdf
	- [ ] Create script to check pdf (python based)
	- [ ] Collect metadata from upload pdf (e.g., page numbers)
	- [ ] Write metadata to PostgreSQL db `metadata`

5. Create basic (local) website with functionality
	- [ ] Show randomly sampled and non-deposited article
	- [ ] Show counter of remaining articles to be liberated
	- [ ] Implement upload procedure
	- [ ] Implement deposit procedure
	- [ ] Allow for implementation into larger website

6. Test deploy of basic website
	- [ ] Deploy PostgreSQL
	- [ ] Deploy Django/Flask

7. Prettify website
	- [ ] CSS style
	- [ ] 

8. Deploy for production
	- [ ] Heroku deploy

9. Communicate launch
	- [ ] ???

### Contributor guidelines

See the [README file](README.md)