---
name: onboard-to-market
about: Introduce a new market-produkt into the axonivy-market
title: Onboard [name] to Axon-ivy market
labels: ''
assignees:
  - ivy-rew
  - alexsuter
  - ivy-lmu
  - andreasbalsiger

---

Hi, I've just created a market-product that I'd like to publish into the official axonivy-market. 
Can you fork it and review my cool product?
[link-to-your-product-repo]



* * *
⚠️ do not remove this section, but leave it to track the reviewer's work.

# Review Tasks

## Product Domain

- [ ] product successfully installs into the Axon Ivy Designer
- [ ] product parts are marked as `Connector` or `Demo`
- [ ] the product projects contains documentation to explain the functionality or use-case: 
   e.g. `Process-Notes`, `Input-Parameter` descriptions, Meta-Comments on `variables.yaml` definitions ...
- [ ] the product readme fits into the market landscape @andreasbalsiger
- [ ] all mandatory setup steps to run the Demo are documented in the setup section of the `[myProduct]/product/Readme.md` .

## Technical Solution

### Coherent

- [ ] Common group-id for all artifacts `<groupId>[org.arcme|com.axonivy].[util|connector].[product-name]<groupId>`
- [ ] Common artifact-id prefix: `<artifactId>msgraph[-product|test|demo]</artifactId>`
- [ ] Html-Dalogs depend on suggested 'frame' template
- [ ] Github actions + maven-build runs as outlined in market-product template

### Maintainable

- [ ] Dependent third-party infrastructure (e.g. Database, MavenRepos) is available: public accessible instance or shared as code (e.g. Docker, docker-compose)
- [ ] Tests are implemented that verify, that the product actually runs
- [ ] Additional libraries (e.g. Maven dependencies) are lightweight: not duplicating libaries of the `Axon.ivy Classpath Container`.
- [ ] Depends on standard Axon Ivy features and does not light-heartedly re-introduce forks of existing solutions (e.g. Job-Framework). Our goal is to integrate also third-parties into existing: Enginge-Cockpit-View, Log-Channels, Monitoring features, ...
- [ ] Uses latest ivy-environment: e.g. process-files and used project-build-plugin match the ivyProject version.
- [ ] Product is re-usable without the need to unpack and customize it for standard use-cases: crucial settings can be overriden with well documented `config/variables.yaml`

