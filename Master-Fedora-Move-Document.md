# First draft of schedule for PHX2 -> IAD2 move

MVFE- Minimal Viable Fedora Environment
PHX2 - Chandler Arizona datacentre
RDU-CC Morrisville NC datacentre community cage
IAD2 - Ashburn Equinix datacentre

### Shipment Equipment

The following lists cover the hardware which is being shipped at specific dates and where the hardware is going.

#### April 13 Cloud to RDU-CC
| Serial No | Model | Mac Address  | Current Hostname | New Hostname |
| --------- | ----- | -----------  | ---------------- | ------------ | 
| NX0217070118 | juniper | ??? | | |
| PE3715270604 | juniper | ??? | | |
| 72000144161487 | OpenGear | ??? | rack 156 open | opengear02.rdu-cc. |
| 3PAC-A0001E | Mustang | ??? | ??? | ??? |
| 3PBC-A00016 | Mustang | ??? | ??? | ??? |
| 2123A7A | Power8 | ??? | ??? | ??? |
| BM3RS13 | Dell R6550 | ??? | copr-vmhost01 | copr-vmhost01 |
| BM4KS13 | Dell R6550 | ??? | copr-vmhost02 | copr-vmhost02 |
| BM4MS13 | Dell R6550 | ??? | copr-vmhost03 | copr-vmhost03 |
| BM4LS13 | Dell R6550 | ??? | copr-vmhost04 | copr-vmhost04 |
| J300MBLP | Len Ampr | ??? | cloud-a64 | cloud-a64 |
| 5MHHS13 | Dell R7550 | ??? | retrace03 | ???? |
| 6KFBR22 | Dell R630 | ??? | ??? | cloudvmhost-x86_64-01 |
| 8KRW842 | Dell R630 | ??? | ??? | cloudvmhost-x86_64-02 |
| 9D15SD2 | Dell FX | ??? | lots-o-stuff | lots-o-stuff |
| NX0217080035 | juniper | ??? | | |
| PE3716010224 | juniper | ??? | | |
| TA3717020687 | 10g switch | ??? | | |
| 2123A6A | Power8 | ??? | ??? | ??? |
| 00D0-0803-001E-31F1-8200-8000 | Cavium 1 | ??? | ??? | ??? |
| 0090-0C03-001E-31F1-8200-8000 | Cavium 2 | ??? | ??? | ??? |
| D149GK2 | Dell FX | ??? | lots-o-stuff | lots-o-stuff |
| E00977 | Storinator | ??? | storinator01 | storinator01 |


#### April 13 MVF to IAD


| Serial No | Model | Mac Address  | Current Hostname | New Hostname |
| --------- | ----- | -----------  | ---------------- | ------------ |
| 72000144161487   | OpenGear | ??? | rack 146 open | opengear01.rdu-cc. |
| 8KRV842 | Dell R630 | B8:2A:72:FC:ED:22 | fed-cloud12 | vmh-x64-09.iad |
| 8KPW842 | Dell R630 | B8:2A:72:FC:F2:2E | fed-cloud13 | vmh-x64-10.iad |
| J300MBV2  | Len Ampr  | E8:6A:64:39:18:99 | vhm-a-22    | vmh-a64-01.iad |
| J300MBPW  | Len Ampr  | E8:6A:64:39:18:85 | vhm-a-21    | vmh-a64-02.iad |
| 1VHTMN2   | Dell R430 | ??? | sign02 | sign02 |
| 1VH7CP2   | Dell R430 | ??? | bkernel04 | bkernel04 |
| 3PBD-A0000Z | Mustang | ??? | ??? | ??? |
| 3PBD-A0004P | Mustang | ??? | ??? | ??? |
| 130C7BA | Power9 | ??? | ??? | ??? |
| 212311A | Power8 | ??? | ??? | ??? |
| J300VGN1  | Len Ampr  | E8:6A:64:97:6B:49 | oqa-a-02    | oqa-a-01.iad |
| 1483H13 | Dell R640 | ??? | ??? | vhm-qa-01.qa |
| 1490H13 | Dell R640 | ??? | ??? | vhm-qa-02.qa |
| 1491H13 | Dell R640 | ??? | ??? | oqa-x86-01.qa |
| 8KQV842 | Dell R630 | ??? | fed-cloud-15 | oqa-x86-02.qa |
| 130FV3A | Power 9 | ??? | ??? | oqa-p64 |
| 869ZLR2 | Dell R630 | ??? | virthost05 | bvhm-02 |


#### June 1st Fedora to IAD

| Serial No | Model | Current Hostname | Current Rack | New Rack | New Hostname |
| --------- | ----- | ---------------- | ------------ | -------- | ------------ |
| J300VGN1 | Ampere | J300MBPW | Rack 150 | 1 | ??? |
| J300MBMH | Ampere | J300MBV2 | Rack 147 | 1 | ??? |
| 8KPW842 | Dell R630 | fed-cloud13 | Rack 157 | 1 | ??? |
| 1VHTMN2 | Dell R430 | sign02 | Rack 148 | 1 | ??? |
| 1VH7CP2 | Dell R430 | bkernel04 | Rack 150 | 1 | ??? |
| 3PBD-A0000Z | Mustang | 3PBC-A0000Z | Rack 146 | 1 | ??? |
| 3PBD-A0004P | Mustang | 3PBD-A0004P | Rack 146 | 1 | ??? |
| 130C7BA | IBM Power 9 | 130C7BA | Rack 147 | 1 | ??? |
| 212311A | IBM Power 8 | 212311A | Rack 147 | 1 | ??? |
| 8FVCGB2 | Dell R630 | virthost02.stg | Rack 153 | 2 | ??? |
| CLTDMN2 | Dell R630 | virthost01.stg | Rack 153 | 2 | ??? |
| 869ZLR2 | Dell R640 | virthost05 | Rack 154 | 2 | ??? |
| 8694MR2 | Dell R640 | virthost04 | Rack 154 | 2 | ??? |
| 8D3NCH2 | Dell R630 | virthost06 | Rack 153 | 2 | ??? |
| 8KQW842 | Dell R630 | virthost02 | Rack 153 | 2 | ??? |
| 1VHVMN2 | Dell R430 | sign01 | Rack 148 | 2 | ??? |
| 6CHVC42 | Dell R630 | backup01 | Rack 155 | 2 | ??? |
| 1VHVMN2 | Dell R430 | sign01 | Rack 148 | 2 | ??? |
| 2LTSCP2 | Dell R730 | virthost01 | Rack 153 | 2 | ??? |
| CKTFMN2 | Dell R630 | virthost12 | Rack 155 | 2 | ??? |
| FH94S52 | Dell R630 | virthost22 | Rack 154 | 2 | ??? |
| 8KQV842 | Dell R630 | fed-cloud15 | Rack 157 | 2 | ??? |
| 60ZG282 | Dell R630 | bvirthost01  | Rack 148 | 2 | ??? |
| 8D3PCH2 | Dell R630 | bvirthost04 | Rack 149 | 2 | ??? |
| 1Q2ZHK2 | Dell R630 | bvirhost05 | Rack 149 | 2 | ??? |
| CLTLMN2 | Dell R630 | bvirthost13 | Rack 149 | 2 | ??? |
| CLTKMN2 | Dell R630 | bvirthost14 | Rack 149 | 2 | ??? |
| CLTGMN2 | Dell R630 | bvirthost15 | Rack 149 | 2 | ??? |
| 1VH6CP2 | Dell R430 | bkernel03 | Rack 150 | 2 | ??? |
| CLTHMN2 | Dell R630 | virthost14 | Rack 154 | 2 | ??? |
| DVT7S52 | Dell R630 | virthost19 | Rack 154 | 2 | ??? |
| DVTS52 | Dell R630 | virthost21 | Rack 154 | 2 | ??? |
| CLSLMN2 | Dell R630 | autosign | Rack 149 | 2 | ??? |
| 2VLSHB2 | Dell FX2 | Builders FX | Rack 150 | 2 | ??? |
| 130FV3A | IBM Power 9 | 130FV3A | Rack 152 | 2 | ??? |
| 21230EA | Ibm Power 8 | 21230EA | Rack 147 | 2 | ??? |
| 130C7AA | Ibm Power 9 | 130C7AA | Rack 147 | 3 | ??? |
| J300MBR6 | Ampere | J300MBR6 | Rack 147 | 3 | ??? |
| J300T2ZA | Ampere | J300T2ZA | Rack 157 | 3 | ??? |
| J300MBPW | Ampere | J300MBPW | Rack 149 | 3 | ??? |
| GIH1P9812A0023 | Cavium | GIH1P9812A0023 | Rack 146 | 3 | ??? |
| J300MBT5 | Ampere | J300MBT5 | Rack 147 | 3 | ??? |
| J300MBMR | Ampere | J300MBMR | Rack 147 | 3 | ??? |
| J300MBRT | Ampere | J300MBRT | Rack 147 | 3 | ??? |
| J300MBLT | Ampere | J300MBLT | Rack 149 | 3 | ??? |
| J300MBRX | Ampere | J300MBRX | Rack 149 | 3 | ??? |
| J300MBNG | Ampere | J300MBNG | Rack 150 | 5 | ??? |
| J300MBLV | Ampere | J300MBLV | Rack 150 | 5 | ??? |
| J300MBNT |  | J300MBNT | Rack 150 | 5 | ??? |
| J300MBRH | Ampere | J300MBRH | Rack 150 | 4 | ??? |
| DVT6S52 | Dell R630 | virthost04.stg | Rack 154 | 4 | ??? |
| 8KRT842 | Dell R630 | virthost03.stg | Rack 153 | 4 | ??? |
| J300MBV2 | Ampere | J300MBV2 | Rack 149 | 4 | ??? |
| CLTJMN2 | Dell R630 | vhost-comm01 | Rack 152 | 4 | ??? |
| 8693MR2 | Dell R640 | qa01 | Rack 151 | 4 | ??? |
| J300MBMN | Ampere | J300MBMN | Rack 147 | 4 | ??? |
| J300MBP4 | Ampere | J300MBP4 | Rack 147 | 4 | ??? |
| J300MBR6 | Ampere | J300MBR6 | Rack 147 | 4 | ??? |
| J300VGMZ | Ampere | J300VGMZ | Rack 150 | 4 | ??? |
| 2VLRHB2 | Dell FX2 | Builders FX | Rack 148 | 4 | ??? |
| 844BE8A | IBM Power 9 | 844BE8A | Rack 152 | 4 | ??? |
| 21230FA | IBM Power 8 | 21230FA | Rack 147 | 4 | ??? |
| ????    | OpenGear | Serial | Rack 146 | 5 | ??? |
| 3PBD-A00053 | Mustang | 3PBD-A00053 | Rack 146 | 5 | ??? |
| 3PBD-A0009P | Mustang | 3PBD-A0009P | Rack 146 | 5 | ??? |
| 3PBD-A0009B | Mustang | 3PBD-A0009B | Rack 146 | 5 | ??? |
| 3PBD-A0002B | Mustang | 3PBD-A0002B | Rack 146 | 5 | ??? |
| 3PBD-A0008J | Mustang | 3PBD-A0008J | Rack 146 | 5 | ??? |
| 3PBD-A0006W | Mustang | 3PBD-A0006W | Rack 146 | 5 | ??? |
| 3PBD-A0004G | Mustang | 3PBD-A0004G | Rack 146 | 5 | ??? |
| 3PBD-A0007T | Mustang | 3PBD-A0007T | Rack 146 | 5 | ??? |
| 212310A | IBM Power 8 | 212310A | Rack 147 | 5 | ??? |
| 844BE8A | IBM Power 8 | 844BE8A | Rack 152 | 5 | ??? |



### Week 00 (2020-03-02 -> 2020-03-08)
 - [x] Hardware shipping needs to be planned out
 - [x] Rack layouts for IAD2 and RDU-CC need to be finalized
 - [x] Work with RH IT on what they need in network diagrams
### Week 01 (2020-03-09 -> 2020-03-15)

 - [x] Get RHEL-8 virthost built
 - [x] Deliver network diagrams to RHIT
 - [x] Announce at downtime for communishift 
 - [x] ~~Try to find a place for communishift to temp run? - no~~
### Week 02 (2020-03-16 -> 2020-03-22)
 - [x] 2020-03-17 Fedora 32 Beta Date
### Week 03 (2020-03-23 -> 2020-03-29)
 - [x] Re-Announce downtime for communishift 
 - [x] Get updated tasks and timeline set out
 - [x] Work out COVID-19 Contingencies
### Week 04 (2020-03-30 -> 2020-04-05)
 - [x] Virthost03 skunkworks (kevin)
     - [x] RHEL-8 install
     - [x] test encryption over bridge
     - [x] test TEAM network
 - [ ] Virthost05 skunkworks (kevin)
     - [ ] uefi EL8 install instructions
     - [ ] secure boot. 
 - [ ] Create template DHCP for mgmt hosts 
 - [ ] Get network layout for RDU-CC finalized
     - [ ] public ip address count and space needed
     - [ ] mgmt network 172.23.1.??/24 
     - [ ] private network for openshift backnodes 172.23.2.??/24
     - [ ] setup a bastion host
         - [ ] ssh
         - [ ] https
         - [ ] tftp
         - [ ] dhcp 
         - [ ] chrony
         - [ ] unbound
         - [ ] general phx2
     - [ ] communishift proxies with private + external interfaces  
 - [x] Work with IT on any network layout issues left for site.
 - [ ] Write howto on Dell mgmt setup (smooge)
     - [ ] set ip address in mac
     - [ ] set up admin user
     - [ ] set ipmi and serial over lan access
 - [ ] Collect all mgmt mac addresses
 - [ ] Collect all hardware mac addresses for debugging
 - [ ] Set mgmt interfaces to DHCP before getting shipped
     - [ ] opengear
     - [ ] amperes
     - [ ] power hardware
 - [ ] Re-Announce downtime for communishift 
 - [x] Set up noggin instance in AWS to replace communishift (kevin)
 - [ ] Work out temporary root password for installs
### Week 05 (2020-04-06 -> 2020-04-12)
 - [ ] 2020-04-07 Fedora 32 Final Freeze
 - [ ] MVFE base hardware and networking should be available in new cage
 - [ ] Set up mgmt interfaces in IAD2
 - [ ] Configure and build out build systems at IAD2
   - [ ] database servers
   - [ ] build hosts
   - [ ] koji
   - [ ] compose systems
   - [ ] etc/etc
 - [ ] Begin takedown of communishift hardware
 - [ ] Power needs to be ready in RDU-CC cage
 - [ ] Build out minimum operating systems on hardware
     - [ ] Install RHEL-8 via drac
     - [ ] Setup bridge interfaces
 - [ ] Configure and build specific services:
     - [ ] bastion
     - [ ] config-mgmt (batcave)
     - [ ] dns
     - [ ] noc/dhcp
     - [ ] log-server
     - [ ] tang
### Week 06 (2020-04-13 -> 2020-04-19)
 - [ ] Communishift 13th April - 1st May 
     - [ ] Power off systems in racks
     - [ ] Work with logistics for pack and move
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
   - [ ] instructions on how to install openshift. 
 - [ ] Move final virthost-cc boxes into new RDU-CC racks
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

### Week 10 (2020-05-11 -> 2020-05-17) 
 - [ ] Change Fedora DNS to shorter times for major change
### Week 11 (2020-05-18 -> 2020-05-24)
 - [ ] Final checklist and approval of IAD2 MVFE 
   - [ ] Test email routing through IAD2 proxies
   - [ ] Test www proxies
   - [ ] Test builds
   - [ ] Test openvpn
   - [ ] Test rsync
   - [ ] Test route to s390x
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

