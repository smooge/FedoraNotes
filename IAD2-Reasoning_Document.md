# Fedora Infrastructure Move from Phoenix to Washington DC
## Background: 
The Fedora Infrastructure houses most of their servers in a sub-cage of the Red Hat Infrastructure main cage in Chandler Arizona. This facility is usually called PHX2 as Red Hat uses a number system of the nearest airport, and then how many facilities. The Fedora Project was originally housed in the PHX1 facility but moved to PHX2 in 2009. The cage was done via a sub-lease which came up in 2019. It was decided not to renew and work began on moving hosts out of the data center. An earlier attempt to move Fedora in the Fall of 2019 did not succeed due to various conflicts. Instead it was decided to move Fedora with the rest of the core Red Hat IT to a new facility they were standing up. This will happen in mid 2020, with the cage to go power dark and be torn down for a new tenant around August. 

The new facility is at an Equinix facility outside of Washington DC, with the nearest airport being Dulles so the code IAD2 is used. Due to the scheduled release of Fedora 32 and its effects on RHEL-8.4 and RHEL-9 alpha, the earliest that Fedora could move its systems would be June 1st. Planning to do this move was begun in late 2019 with various teams working out high level logistics. In December, technical details and logistical requests from Equinix were started to be worked out. 
Goal:
The end goal of this project is the moving of the Fedora Infrastructure from Phoenix to IAD2 with normal operations of builds and other services by 2020-07-01 (July 1st 2020). To meet this goal, considerations need to be made on
Minimum operations are possible from late May (2020-05) to June while equipment is shut down, packed and shipped across the country.
Maximum amount of hardware must be able to move from PHX2 to IAD2 with minimum amount of failure or destruction.
Alternative plans on what to do with failure or loss need to be documented, agreed upon and followed. 
Timelines and detailed deliverables need to be clear from all sides so that agreements can be made quickly.
Site Considerations:
Various items have been found out about the IAD2 facility which raised concerns that needed extra research:
PHX2 uses US 220V 60 Hz power. The IAD2 facility uses EU 240V 50 Hz power. In the past this required physical changes to power supplies of servers (usually a little switch on the back or on top of the internal power supply). This was different from laptops which have sensors to autochange to power hertz changes. Most modern power supplies no longer need this physical change.
PHX2 contains 12 42 U racks for all of Fedora Infrastructure, Fedora QA, and Fedora Cloud. However many of the racks are 50% full to allow for future growth. 
IAD2 was to have 6 52 U racks for all of Fedora and its storage. Racks and PDUs are charged in a way for maximum capacity so having a 50% full rack means that money is being charged for power not being used. 
There was some early confusion on that we thought we would be able to lease an outside of the cage rack, but the OPEX pricing came back as too much for IT to spend on. 
Cooling at PHX2 uses below floor forced air. Air is pushed from the sides of the rooms through chillers which force the air under the floor. This then comes up in front and under the computers to help cool the systems. The air then circulated back to the side pumps
Cooling at IAD2 does not use below forced air. It instead uses a different side to side airflow where the air is chilled on one side and then pulled out at places above the floor. This changes how systems cool in racks and depending on where the chiller is could require multiple spacers above systems with more than 6 drives. [Many Fedora servers have 8 to 10 drives.] This raised concerns as putting the spacers in dropped our ability to use the 5 racks efficiently. 
PHX2 uses Red Hat contracted on-site staff to install, rewire, change systems. This has meant that our work methods have allowed us to have short lead-time for racking new hardware or changing existing hardware. 
IAD2 will use Equinix staff to rack and stack and do trouble tickets. This will require longer lead out times for changes and fixes. A general estimate on racking and stacking a system is over a week from delivery unless an expedited ticket is put in. All of these seem to be on a charged basis. 
Because the IAD2 system uses a different contracter system for rack and stack, more detailed wiring and elevation plans are required. At PHX2 our tickets tend to say ‘put in Fedora area where there is room, wire to top of rack switch, and let us know which ports so we can get Matt Galgoci to change vlans. At IAD2 a detailed elevation (aka which rack, which U, what type of mounting, which power, and which network switch and port is needed. As Equinix has multiple facilities, customers and projects, they also need these documents on specific dates or rollouts can cascade out weeks as higher priority work comes in.
Move Considerations:
For the last 10 years, Matt Galgoci has been our ‘goto’ person to fix all our networking issues. If we wanted a port changed to a different vlan, a different firewall rule, or a dozen other things, we would send an email to servicedesk and Matt and he would fix it as soon as he could. This also caused problems at times when Matt wasn’t available or someone else tried to help. Changes in how this works have been in the works, and for IAD2 all networking changes will need to go through standard IT processes. This means more planning, putting in change requests, and possibly presenting at ITIL type meetings.
In order to deal with SPAM and some other concerns from a security incident, all Fedora email has been routed through Red Hat’s email firewalls for the last 10+ years. This has been done through various firewall rules and other routing. As such we have been the ‘number’ one user of the email systems. Red Hat is changing how its mail routing and filtering to a SaaS provider which seems to  charge per email filtered. In previous move attempts, Fedora has been expected to take up filtering our own email. We have pushed back on it as that is a large service.
Previous planned upgrades in 2012 and 2016 for the PHX2 site were to bring in IPv6 and 10 gigabit networking between hosts. Fedora began buying 10gig ready systems for the last 4 years so that nearly all systems are able to be 10gig ready. However 10 gig networking is not as ‘cheap’ in material as 1 gigabit networking. We have 3 10 gig switches already and we're expecting that each rack would come with 1 or more 10gig for the new networks. However, there was some miscommunication on this.
Fedora has a 6 month release cycle which means we produce a release around October 31st and May 15th. This release is then used as the basis for various RHEL releases with Fedora 32 in May being required for starting RHEL-9 deliverables. This means that downtimes for certain services must be short and planned so that other groups can know they will be affected. This made it so that Fedora could not move before June 1st and really needed to be available sometime in late June or July. 
Many internal groups use internal links to the Fedoraproject download servers for product lines. Changes to these hostnames, firewall rules, routing, etc will need to be found and adjusted. Communication to PnT and other groups usually needs multiple iterations over 3-4 months. 
Red Hat Legal uses a CentOS git server in PHX2 to help meet export compliance rules for Fedora, RHEL and other products to be available to users or customers. A new server in IAD2 will need to be set up before the PHX2 can be down, and legal must make appropriate paperwork changes.
Moving hardware takes time. Each Fedora rack will take at least 4 hours and up to a full business day to remove all the systems and put them in cross country shipping. From our just moving systems across the cage in 2017(?), only two racks can be worked on at a time with 2 teams. As such, we are looking at best 3 days to derack hardware]. The shipping across the United States will usually take 5 business days. Equinix gives a 3 day turnaround time for expedited rack and stack and 3 weeks for regular rack and stack. 

Known Deadlines:
Fixed:
2020-01-31 - Wiring and Elevation charts need to go to Equinix
2020-02-28 - Fedora Cloud needs to decommission ip addresses
2020-04-15 - Stage 1 systems turned off in PHX2 and ship to IAD2
2020-05-01 - Stage 1 systems arrive in IAD2 and get installed.
2020-06-01 - Fedora PHX2 goes offline to move
Variable:
2020-04-Early - IAD2 Cage should have power on and rack 101 should be available
2020-04-Early - IAD2 Stage 0 systems are installed and testing begins
2020-05-Mid - Fedora 32 is released
January Deadlines
The current plan on Red Hat IT side was to have the cage ready for initial tenants in April. With other moves and considerations this would allow us to stand up an initial rack so we could move in June. However, to meet that April deadline, Equinix needed plans for elevations, power, network, and other things by January 27th with a slack time of February 3rd. Any deviation would move the buildout by a month or more for the Fedora part of the cage. 
Work Completed By January 31st:
Determine which systems would be shipped and which ones needed to be retired. 
Determine that all systems being shipped are 240V/50Hz capable. All Dell systems should autoswitch but some of the older ones may experience power supply failures due to age. Cavium and Ampere systems should also autoswitch. IBM Power PC ‘should’ but they are lab loaner systems so may also have some failures. Mustang systems ‘should’. If they fail we do not replace.
Cooling changes. Red Hat IT will purchase sensors to put in each rack and are paying for 2U front-to-back fans which will be used to help push air through each rack. Rack elevations were changed so that hot systems are on the bottom with spacers. 
Wiring laid out. Red Hat IT’s Chris Addair made power maps for all the systems, and Stephen Smoogen worked out network mapping for all systems.
Additional switches requested. Matt Galgoci and Stephen Smoogen presented reasoning for why additional 10 gig switches were needed. Seth Shevach is taking to CIO/CFO for final approval but thinks it meets appropriate reasons. Only 2 10 gig switches will be available for initial buildout in April. This means all buildout systems need to go into 2 racks (Rack 101 for systems and Rack 106 for storage).
Racks will be tight on available ports. Additional switches may need to be purchased by Engineering in the future.
February Deadlines
The move has a lot of moving parts and even though we will not be able to set up any systems at IAD2 until April, we need to put a lot of things together so that when we get to that date we can meet our May and June shipping dates. The following is a set of things I believe need to be looked at and dealt with by February 28th.

AARCH64 system changes in PHX2. We purchased multiple Ampere aarch64 systems last Fall to replace our aging HP Moonshot. Due to timing and wiring delays we have not been able to get these installed. These need to be installed so that we can turn off the HP Moonshot before May.
Locate systems still needing installation
Update their BIOS/configs to latest
Go into Red Hat IT DCIM and find ports on switches
Get switches all turned onto appropriate vlans
Install el8 onto each system
Move vms from moonshot
Turn off moonshot so IT can decommission. 
Rebuild virthost03. System was rebuilt to deal with broken signhost. Then it was rebuilt to try and work with local disk encryption + tang. We found that grub+tang does not work with bridge interfaces so the server would only reboot properly every now and then.
Rebuild with rhel8
Put in rotation to take vms from other hosts
COPR. The COPR build system is used for both internal and external development and has been living in the Fedora Cloud for a number of years. The hardware and OS it is using are EOL and need to be replaced. 
Find out where COPR PO order went. A set of systems to replace older IBM boxes that COPR uses for its master were put into the order system in January. They never got ordered and so we can not move COPR out of the cloud.
Move COPR to new hosts. Either get them onto boxes which have been ordered or temporarily onto rebuilt cloud nodes.
Move COPR storage off of Equallogics.  COPR is currently stored on several Equallogics in PHX2 cloud network. Backend storage is ‘blocked’ on a specific network and copying data from it has been slow to non-existent due to that. Equallogics need to be taken off Fedora Cloud Network and put on the same network as the 45drives. 45drives then needs to iscsi mount this and all data needs to be synced over. [Take about 4 days.] 
Turn off old IP space in Fedora Cloud by 2020-02-28. The original Fedora cloud was using a netblock that was meant for other projects. We got a replacement netblock a while ago, but because of the failure of getting newer OpenStack installed were not able to transition to it. Red Hat IT requires that network block turned over to them by March 1st, 2020 so that they can stand up parts of the networks at the new facility. [Due to the age and problems with the old cloud it may be best to turn it off.. Period.]
Install QA virthost-comm replacement boxes. Boxes to replace out of warranty systems were gotten in December. They arrived and were put in racks 2 weeks ago. Getting the network ports wired and ready gets older hardware turned off sooner.
Locate systems still needing installation
Update their BIOS/configs to latest
Go into Red Hat IT DCIM and find ports on switches
Get switches all turned onto appropriate vlans
Install el8 onto each system
Move vms from old vhost-comm
Turn off old vhost so IT can decommission. 
Get new network requirements mapped out. Currently Fedora has 8 vlans (or security zones in the current networking parlance). Most of these have a hodgepodge set of firewall rules between them which require constant updating as new services are brought online. Networking would like for us to consolidate down our network space to a more manageable set and also to have the rules available for review and testing. 
What zones do we have and do we still need them?
What are the exceptions we have and do we still need them
What are the tools and exceptions that Red Hat business units have with us so that they can continue working?
What hosts will we be NATing at new location
How will things talk to each other.
Determine if we need to keep certain security holes in place [Secondary SSH etc]
How many networks do we need and what their ip ranges will be.
Get ironed out networking rules between IAD2 and PHX2. The assumptions that we have and networking and storage and security do not seem to match up.
Determine if we need to stand up additional SMTP services. This is mainly to make sure that no one is assuming we are doing one thing and we do another. Or if we are required to change, who is paying for it and how. We will still need to work out SMTP routing through various firewalls.
Map out exactly what is needed to be run in the MVP. The new location will require us to give new ip addresses to every system. It will also require us to change hostnames, firewalls and many other things. It also can not run every service we currently run in Fedora. Some things will have to be temporarily put on hold and others may be ended altogether. 
Begin communication about outage and its effects on Fedoraproject. This is going to be a 6 month long project and will have small effects all the way through the move. Many people who are going to be affected only check what is going on in a haphazard fashion. We will need to communicate clearly and regularly what is going on.
Work Completed by February 15
To be filled out later
Work Completed by February 29
To be filled out later
March-July Deliverables:
There are a large number of additional deliverables but their exact dates for being needed are not set at this time. As such, I have listed them below as work that will be filled out as time proceeds.
General:
Contact vendors about move plans. Need to work out with 45drives, IBM PPC, Lenovo Ampere, and Dell on how to safely move hardware from one location to another.. Also prepare any additional ‘spare’ equipment at the destination site at move dates so repairs can be made quickly. 
Map out DNS for new IAD2 networks. DNS is the database which is used to map computer IP addresses to names that people and configuration files can remember. Currently the system uses a templating script written before 2012 by Seth Vidal. Its logic is hard-coded to work with things being in PHX2 and networks being in certain ways. We need to work out a new script/template system which we can feed info from ansible hosts data. 
Map out DHCP for new IAD2 networks. DHCP is used by systems to boot up, set their initial IP address, and know where certain resources are from. This is tied into the DNS but is a separate service. Currently the file is hardcoded spaghetti code with settings grandfathered in over 14 years. New version will only allow for some ips to boot to them as temporary ips.
Set up TFTP system for the new IAD2 network. This service is used for initial setup of systems while they are booting. The hardware will request certain files which are then to boot and build the system. Current system is half templated and half spaghetti hard code.
Determine if changes or additional OpenVPN networks are needed. Fedora uses OpenVPN for potentially unprotected transfer of data from various hosts inside and outside of PHX2. Moving the VPN primary routes always has knock-on effects which need to be examined and worked out.
Set up monitoring templates for the new IAD2 network. In order to know what services are running or not in the new datacenter. Currently we are using a templated system for Nagios which should be hackable into the new center.. However I do not know how long that will take.
Set up mail routing for the new IAD2 network. These will be configuration files that will sit on our bastion hosts to accept email from the world and internally and route to the appropriate sites. Certain internal sites have hard-coded acceptance from old Fedoraproject ips which will need to be updated. Other spam and other rules will need changes. 
Test and deploy initial systems in IAD2. Red Hat IT bought systems to replace ones we could not move from PHX2 due to warranty and age. These systems will be called Stage 0 and will be used as part of the Minimum Viable Project (MVP), and will need to be set up and added.
Test initial management network settings with Red Hat IT
Set up Stage 0 management ip addresses.
Update BIOS/Firmware on each Stage 0 box. [This helps test network conductivity and removes a stage later.]
Remote install minimum operating system to run virtual machines on hardware. Test that networks are reachable and work. Make changes as needed.
Install minimum needed virtual guests so that other work can be done.
Bastion host to talk to internet or other restricted networks. Test protocols to be proxied:
SMTP
SSH
OpenVPN
DNS/DHCP/TFTP host(s) to give data needed for other systems to boot.
Batcave host to run ansible from 
Monitoring host to tell about problems 
Tang host to allow encrypted systems to boot up
Set up other virtual server hosts on specific networks (QA, build and Red).
Test network for readiness and complete signoff
Ability to mount and use NFS from Netapp.
Netapp file system snap mirroring from PHX2, RDU2 and IAD2
Testing shares for ‘MVP’ set up on Netapp and synced from PHX2.
Mirroring software from RHN into batcave3
Ability to talk across networks to PHX2 and IAD2 without using openvpn?
Move initial systems from PHX2. In order to have enough hosts in IAD2 to set up a working Minimum Viable Project (MVP), hosts which are currently in use will need to be moved before the main move. In order to do this, we will need to:
Identify which hosts are being moved. [Initial list was done in January to meet rollout schedule.]
Communicate that services will be compacted and outages or slowness is to be expected.
Lower cpu/memory usage on systems which are staying. This is needed for the next stage:
Move virtual machines off of to-be-moved systems. 
Clear off servers so that they do not start ‘talking’ on the wrong networks at new site.
Schedule shipping and movement of systems with Red Hat IT.
Test Backups and Recovery. Restore systems from scratch (aka rebuild initial box, restore from rdiff-backup, bring online, document process and confirm working.)
Move Stage 1 systems from PHX2. As initial systems in PHX2 are shipped and ready, bring them up in IAD2. Add the minimum viable guests to the system as needed. 
Bring system onto network and reconfigure mgmt interface.
Set up network ports appropriately
Rebuild server as needed.
Set up guests as needed
Bring up MVP at IAD2 (2020-04-15?). Initial plan would be to bring up MVP like it was another ‘staging’ network of PHX2. It copies all the services but none of them are considered primary and things could be resynced over at any time. Services would be then tested that things worked as needed.
Confirm that builds can be done
Confirm other services
Communicate clearly that these are the only services which will be available during move.
Fedora 32.
Continue work on Fedora 32 at PHX2. As much as possible continue with things like they are with a Freeze on infrastructure changes in late April and early May.
Release Fedora 32 around May 15.
Move builds to emergency only around May 31st. 
Change global DNS to shorter time settings. DNS works by setting ‘timeouts’ for how long a server should ‘keep’ hold of old data versus checking. Because IP addresses will be moving, it is always needed that a month before the move to change the timeouts to be 24 hours for some and 1 hour for others.
Begin ramp down and transfer over to IAD2. As Fedora 32 gets out to mirrors, we will begin ramping down the services in PHX2 with a shutdown of May 31st. Services like COPR will go offline and other services will move to a lower availability status.
Map PHX2 systems to new roles. Determine which systems will be redeployed from scratch and which ones will just be a ‘reconfigure of ip addresses’. 
MOVE (2020-06-01)
Final confirmation that all of MVP is working as needed.
Move global DNS to point to new dns servers and ip addresses at MVP
Fix important and high level problems missed 
Turn off PHX2
Bring down servers cleanly. Clean out systems we plan to redeploy and set others servers into a neutral state so that when they come up they will not break MVP if powered on in new network.
Follow vendor provided instructions on getting systems ready for move
Have movers ship hardware
Wait 5 to 11  business days for hardware to go across the country. [Shipping will be expedited but still slow]
Work with Red Hat IT/Equinix to get hardware out of delivery (expect 3 to 5 business days)
Initial racking and power on. 
Bring racked systems into a neutral network setting. This will make sure that nothing spews nonsense on a message bus or something similar. 
Fix hardware problems for systems with warranties. Any systems without warranties being shipped will need to be sent to RDU2 for any ‘work’ that can be done. 
Configure hosts with new ip addresses.
Switch hardware to established networks
Bring online with MVP.
Lather, rinse, repeat.
Move MVP to being a fully operational death star. This will be work which will cover about 3-6 months in a break-fix manner as little problems occur. There will be a higher number of hardware failures in the first 6 months after a cross-country move so this will be something that will take up time.
Deal with PHX2 closeout paperwork and hardware work. Systems left in PHX2 will need to be cleaned and sent to either other sites or sent to a recycler. Paperwork and work on this will need to be done. 
Lessons Learned.
Document, document, document.
