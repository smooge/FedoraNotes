# First draft of schedule for PHX2 -> IAD2 move

MVFE- Minimal Viable Fedora Environment
PHX2 - Chandler Arizona datacentre
RDU-CC Morrisville NC datacentre community cage
IAD2 - Ashburn Equinix datacentre

### Shipment Equipment

The following lists cover the hardware which is being shipped at specific dates and where the hardware is going.

#### April 13 Cloud to RDU-CC


#### April 13 MVF to IAD

#### May 15 OpenQA to IAD

#### June 1st Fedora to IAD

### Week 00 (2020-03-02 -> 2020-03-08)
 - [ ] Hardware shipping needs to be planned out
 - [ ] Rack layouts for IAD2 and RDU-CC need to be finalized
 - [ ] Work with RH IT on what they need in network diagrams
### Week 01 (2020-03-09 -> 2020-03-15)
 - [ ] Collect all mgmt mac addresses
 - [ ] Get networking vlans for new RDU-CC internal network for mgmt
 - [ ] Create template DHCP for mgmt hosts
 - [ ] Set 40 mgmt interfaces to DHCP 
 - [ ] Get RHEL-8 virthost built
 - [ ] Deliver network diagrams to RHIT
 - [ ] also invite them to test when back up
 - [ ] Announce at downtime for communishift 
 - [ ] Try to find a place for communishift to temp run? - no
### Week 02 (2020-03-16 -> 2020-03-22)
 - [ ] 2020-03-17 Fedora 32 Beta Date
 - [ ] Set 40 mgmt interfaces to DHCP 
 - [ ] Re-Announce downtime for communishift 
 - [ ] Get network layout for PHX2 finalized
### Week 03 (2020-03-23 -> 2020-03-29)
 - [ ] Work with IT on any network layout issues left for site.
 - [ ] Set 40 mgmt interfaces to DHCP 
 - [ ] Set up mgmt interfaces in IAD2
 - [ ] Re-Announce downtime for communishift 
 - [ ] Schedule and Move any required communishift items to 'cloud?'
 - [ ] Work out temporary root password for installs
### Week 04 (2020-03-30 -> 2020-04-05)
 - [ ] MVFE base hardware and networking should be available in new cage
 - [ ] Finish mgmt configuration of PHX2 systems
 - [ ] Build out minimum operating systems on hardware
 - [ ] Configure and build specific services:
   - [ ] bastion
   - [ ] config-mgmt (batcave)
   - [ ] dns
   - [ ] noc/dhcp
   - [ ] log-server
 - [ ] Re-Announce downtime for communishift 
 - [ ] Move any required communishift items to 'cloud?'
### Week 05 (2020-04-06 -> 2020-04-12)
 - [ ] 2020-04-07 Fedora 32 Final Freeze
 - [ ] Configure and build out build systems at IAD2
   - [ ] database servers
   - [ ] build hosts
   - [ ] koji
   - [ ] compose systems
   - [ ] etc/etc
 - [ ] Begin takedown of communishift hardware
 - [ ] Power needs to be ready in RDU-CC cage
### Week 06 (2020-04-13 -> 2020-04-19)
 - [ ] Communishift 13th April - 1st May 
   - [ ] box should arrive on 22nd
   - [ ] Power should be on by 17th - this is power to RDU-CC 
   - [ ] Rerack from 27th 1st may
   - [ ] test and good to go by May 8th
   - [ ] Announce to FAS group link
 - [ ] Take down and ship communishift hardware to RDU-CC
 - [ ] Take down and ship extra hardware to IAD2
 - [ ] Configure and build out prod systems at IAD2
   - [ ] proxies
   - [ ] sundries
   - [ ] value
   - [ ] etc/etc
### Week 07 (2020-04-20 -> 2020-04-26)
 - [ ] Hardware should arrive at RDU-CC
   - [ ] work with Shauns team to get racks in place
   - [ ] work with PNT/Shauns team to get systems racked
   - [ ] power up communishift
   - [ ] change ips and other config work
 - [ ] Hardware should arrive at IAD2
   - [ ] work with Shauns team to get systems racked/stacked in 101
   - [ ] begin configuration and set up of moved systems
### Week 08 (2020-04-27 -> 2020-05-03)
 - [ ] 2020-04-28 Fedora 32 first release window
 - [ ] Bring communishift back to full usage. 
 - [ ] Bring COPR and retrace to full usage in RDU-CC
 - [ ] Get SMTP rules 
### Week 09 (2020-05-04 -> 2020-05-10)
 - [ ] 2020-05-05 Fedora 32 2nd release window
 - [ ] Move final virthost-cc boxes into new RDU-CC racks
 - [ ] Take down part of openqa for shipment to IAD2
### Week 10 (2020-05-11 -> 2020-05-17) 
 - [ ] QA infrastructure shipped to IAD2
 - [ ] Change Fedora DNS to shorter times for major change
### Week 11 (2020-05-18 -> 2020-05-24)
 - [ ] Final checklist and approval of IAD2 MVFE 
   - [ ] Test email routing through IAD2 proxies
   - [ ] Test www proxies
   - [ ] Test builds
   - [ ] Test openvpn
   - [ ] Test rsync
   - [ ] Test route to s390x
 - [ ] Get hardware from QA shipment racked to IAD2
 - [ ] Bring up openqa in IAD2
### Week 12 (2020-05-25 -> 2020-05-31)
 - [ ] Move logical infrastructure to IAD2 MVFE
   - [ ] Shutdown PHX2 koji and related dbs
   - [ ] Do final dump
   - [ ] Import data into IAD2 dbs
   - [ ] Turn DNS to point to IAD2
   - [ ] Move openvpn to IAD2
 - [ ] Begin cleaning PHX2 systems as possible 
   - [ ] Reinstall with base EL8?
 - [ ] Power off PHX2 systems as possible
### Week 13 (2020-06-01 -> 2020-06-07)
 - [ ] Shutdown of PHX2 racks
 - [ ] Removal of systems from PHX2 and shipment to IAD2
 - [ ] Travel of equipment to IAD2
 - [ ] PHX2 -- go over remaining hardware to recycle
### Week 14 (2020-06-08 -> 2020-06-14)
 - [ ] Most likely time for hardware arrival
 - [ ] Racking and stacking of IAD2 equipment
 - [ ] Set up mgmt interfaces
 - [ ] Do initial hardware installs to RHEL8
### Week 15 (2020-06-15 -> 2020-06-21)
 - [ ] Finish initial hardware installs 
 - [ ] Bring up additional builders 
### Week 16 (2020-06-22 -> 2020-06-28)
 - [ ] Bring up additional services
 - [ ] Move mgmt interfaces back to static
### Week 17 (2020-06-29 -> 2020-07-05)
 - [ ] Probably more work at data centre
### Week 18 (2020-07-06 -> 2020-07-12)
 - [ ] Sign off on work completed
### Week 19 (2020-07-13 -> 2020-07-19)
 - [ ] A miracle occurs *Several in fact*
### Week 20 (2020-07-20 -> 2020-07-26)
 - [ ] Mass Rebuild for Fedora 33 starts
   - [ ] All systems must be up and running
   - [ ] Production needs to be normal
### Week 21 (2020-07-27 -> 2020-08-02)
### Week 22 (2020-08-03 -> 2020-08-09)
 - [ ] FlockToFedora 2020

