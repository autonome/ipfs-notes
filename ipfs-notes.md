# IPFS Notes

## Meta

* My Zoom URL: https://protocol.zoom.us/my/dietrich.pl
* My Calendly: https://calendly.com/dietrich-pl
* My PL Gravatar: https://en.gravatar.com/userimage/267418/2e9fb5eca838a3599c23a49f86b36771.png

## Vision/Purpose/Why

Value proposition
* use cases
* case studies
* benchmarks

Interesting views
* https://medium.com/offline-camp/decentralization-is-not-enough-75b15b8bc230

Communicating
* https://news.ycombinator.com/item?id=20137918#up_20179612
* how can I measure *my* IPFS usage? eg bandwidth, performance
* how can I measure my IPFS exposure? bandwidth, dht connections, etc

## Current Activities

* Browser integrations
* Metrics
* Collaborations
* IPFS Camp
* Standardization / governance

Themes
* privacy
* offline
* anonymity
* censorship
* performance
* stability

## Playtime

* design basic evite page system that works with email or sms
  * subdomains + localstorage
  * unique invite code per user, transformed into locally-stored key
  * key decrypts data that's synced over... web-rtc data channels? ipfs pubsub?
  * crdt?

* ittybitty on ipfs
* ittybitty filtering search for curated lists

* ProperNew - in a given stream of documents, collect new proper nouns for triage

* simplerme - all my publicness (tweets/tumblrs/insta migrators) all migrated to indieweb -> ipfs
* evite on top of phone contacts on ipfs
* taking phone contacts graph outside the phone, as dweb app framework (eg keys)
* lightweight privacy-oriented and publicly shared metrics framework on ipfs
* research how to do time series data on ipfs? ipns -> cid -> pubsupdates
* IPFS PWA share target (-> publishable)
	* -> screenshot sharing pwa desktop mac chrome share target
* publishable sidebar
  * screenshots?
* sketchlog
* React Native IPFS playground
* conversational interface
* Frame as IPFS-native browser, as registered handler for ipfs protocol
* Multipublish: static publish -> dat/ipfs/ssb/activitypub

## Theory of Change

* https://en.wikipedia.org/wiki/Theory_of_change
* https://en.wikipedia.org/wiki/Capacity_building

## Stacks and Directions

Publish content to network
* pwa base
* js-ipfs
* share target

Publish app to network
* the dns permutations
* sxg
* lunet

## Climate / Power Consumption

From Michelle:

* [How to stop data centres from gobbling up the world’s electricity](https://www.nature.com/articles/d41586-018-06610-y)
* [YouTube's carbon footprint is huge, but smarter web design could fix it](https://www.wired.co.uk/article/youtube-digital-waste-interaction-design)

* https://github.com/mmes2/muse

## Primary Use-cases

Defining the primary user needs addressed by IPFS.

* Saving/Archiving
  * dependencies
    * mfs (blocker)
    * stripping text
  * co-op wins with other WGs
    * offline wg - supports offline viewing of saved content
* Publishing
  * dependencies
    * mfs (blocker)
    * ipns
* Sharing
  * dependencies
    * mfs (nice to have)
    * archiving (blocker)
* Reading
  * access to stored content

Related issues
* [Design: Creating Simple Websites with IPFS](https://github.com/ipfs/ipfs-gui/issues/69)

## Censorship Resistance

* https://www.ischool.berkeley.edu/people/xiao-qiang

## Performance

* https://github.com/ipfs/benchmarks
* can i use testlab to run scenarios? 
* what's the set of information i need?

Issues
* DHT in libp2p: https://github.com/libp2p/go-libp2p-kad-dht/issues/345
* good roundup: https://github.com/ipfs/go-ipfs/issues/6342

IPNS
* [About IPNS and Performance, hackmd mid-2019](https://hackmd.io/yzGOY7UkQ1uMR0tRemQ5yw)
* [IPNS very slow, ipfs/go-ipfs#3860](https://github.com/ipfs/go-ipfs/issues/3860)
* [IPNS resolution takes a long time, forum](https://discuss.ipfs.io/t/ipns-resolution-takes-a-very-long-time-first-time-around/5620/2?u=lidel)
* [IPNS over workers (wip from hugo)](https://github.com/ipfs/js-ipfs/tree/feat/ipns-over-workers)

## Bandwidth Consumption/Savings

* (from homepage) ["With video delivery, a P2P approach could save 60% in bandwidth costs.", 2010](http://math.oregonstate.edu/~kovchegy/web/papers/p2p-vdn.pdf)
* ["Reducing Bandwidth Utilization in Peer-to-Peer Networks", 2003](https://www.researchgate.net/publication/228550567_Reducing_Bandwidth_Utilization_in_Peer-to-Peer_Networks)

* how can I measure *my* IPFS usage? eg bandwidth, performance

* Edgar from Netflix, distributing ubuntu w/ containers

## Debugging

* https://github.com/anacrolix/go-libp2p-dht-tool/

## Criticism

* tom macwright post
* https://www.minds.com/barnumpt/blog/ipfs-the-pied-piper-without-a-flute-1034755524102819840


## Questions, Concerns, Challenges

Real feedback from the real world.

"I can't delete files" - revenge porn, intentional or accidental exposure, sysadmin requests to DMCA takedowns
* Mastodon author Gargron - https://github.com/tootsuite/mastodon/issues/360#issuecomment-300249551

"How do my files stay up?" - the magical promise and the start reality
* "pinning" doesn't make sense to developers - need to use their language
* TODO: Find some good examples

"It's so slow"
* TODO: find those HN and Reddit thread comments

"Makes my laptop hot and pegs CPU"
* TODO: find those HN and Reddit thread comments

"I suffered immensely at the hand of IPFS" - https://devpost.com/software/ethny-tracker
  * "Syncing to an IPFS in-browser node is insufficient for distributing metadata hashes"

CIDs are mutable - if we change chunking default, etc
https://discuss.status.im/t/ipfs-alternatives-snt-utility/1228/5

All API pathways to add a file do not result in same resulting output CID (eg folder etc)


## Archiving

Why
* [Scholarly Context Adrift: Three out of Four URI References Lead to Changed Content](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0167475)

## DAT vs IPFS

* [DAT response to Tom MacWright](https://medium.com/blue-link-labs/so-you-want-your-decentralized-browser-to-work-correctly-c06c4038ab12)

## Misconceptions I had

* I had no understanding of CIDs. At all. I thought IPFS addresses were a much simpler hash.

* I thought IPFS just shared files on disk. I had no idea it *copied* files you added, and kept them in a separate local datastore.

* I had no idea IPNS existed.

* I had no idea that MFS existed.

* I did not know how much of IPFS was actually libp2p.

* I had no idea that JS implementation was not the primary one.


## Use-cases

* Large file hosting
  * [In open source projects / community networks](https://mastodon.social/@Gargron/102449366185658028)
  * [LineageOS ROM hosting](https://lineageos-on-ipfs.com/)
* Local computer use-cases
  * [Using less local disk storage than raw filesystem for game backups](https://www.reddit.com/r/ipfs/comments/cchr8b/whats_the_coolest_thing_youve_seen_done_with_ipfs/)
* Data hosting
  * [thread on r/selfhosted of suggestions for public services to host](https://www.reddit.com/r/selfhosted/comments/ctuzfs/suggestions_for_public_services_to_host/)
* General
  * [thread of things people are doing with IPFS on r/ipfs](https://www.reddit.com/r/ipfs/comments/cchr8b/whats_the_coolest_thing_youve_seen_done_with_ipfs/)

* [Distributed filesystems thread on r/selfhosted](https://www.reddit.com/r/selfhosted/comments/ds0m13/distributed_file_system_options/)

## Projects choosing IPFS or not

Projects re adopting IPFS or not
* [LineageOS on why not IPFS](https://www.reddit.com/r/LineageOS/comments/brnmmd/if_lineageos_team_doesnt_want_to_host_images_for/?depth=2)
* [Blockstack vs IPFS](https://forum.blockstack.org/t/cannot-find-ipfs-driver/6147)
* [Radicle on leaving IPFS](https://github.com/radicle-dev/radicle/issues/689)
* Mastodon
	* https://mastodon.social/@Gargron/102050448708258784
  * https://github.com/tootsuite/mastodon/issues/360
  * https://github.com/tootsuite/mastodon/issues/477

IPFS vs a blockchain
* [XYO on why chose IPFS over blockchain](https://cryptoinsider.com/exclusive-xyo-head-of-community-explains-why-they-chose-ipfs-not-blockchain/)

Specific reasons
* [non-deterministic chunking](https://discuss.status.im/t/ipfs-alternatives-snt-utility/1228/5)

Dat vs IPFS
* [Entropic](https://github.com/entropic-dev/entropic/issues/99#issuecomment-499106368)

Blog posts and rants
* [Tom MacWright - IPFS, Again](https://macwright.org/2019/06/08/ipfs-again.html)
* [HN thread for Tom MacWright post](https://news.ycombinator.com/item?id=20137918)
* https://blog.boramalper.org/what-ipfs-fails-to-address/

## IPFS + Other Dweb Projects

* IPFS + Solid
  * https://github.com/Eximua/solid-ipfs

## Web Standards / Browser Dependencies

Features of Interest

* [Alt-svc](https://github.com/ipfs/in-web-browsers/issues/144)
* [HTTPS-Local](https://www.w3.org/community/httpslocal/)
* [WebRTC-QUIC](https://github.com/w3c/webrtc-quic/)
* Signed HTTP Exchanges
  * [IPFS/IWB](https://github.com/ipfs/in-web-browsers/issues/121)
  * [W3C/Strategy](https://github.com/w3c/strategy/issues/171)
  * [Mozilla's position](https://github.com/mozilla/standards-positions/issues/29)

Gecko issues of interest
* [Add DNS TXT resolution to dns.resolve WebExtensions API](https://bugzilla.mozilla.org/show_bug.cgi?id=1449171)
* [webRequest.onBeforeRequest/onHeadersReceived fetch redirect gets blocked due to bogus CORS error](https://bugzilla.mozilla.org/show_bug.cgi?id=1450965)
* [APIs for p2p web applications](https://bugzilla.mozilla.org/show_bug.cgi?id=1435798)
* [Workers fail to fetch from loopback addresses like http://127.0.0.1](https://bugzilla.mozilla.org/show_bug.cgi?id=1520381)
* [Stop treating "http://localhost/" (by name) as mixed content](https://bugzilla.mozilla.org/show_bug.cgi?id=1488740)
* [new TCPServerSocket should fail if port is already in use](https://bugzilla.mozilla.org/show_bug.cgi?id=1474150)

Chromium
* [webRequest: add property to event data indicating which navigation the resource is for](https://bugs.chromium.org/p/chromium/issues/detail?id=637002)
* [Extensions should be able to register for protocols](https://bugs.chromium.org/p/chromium/issues/detail?id=64100#c12)

Dapps
* [Add dweb.link to public suffix list](https://github.com/publicsuffix/list/pull/766)

mDNS and related
* [Add Network Service Discovery API support](https://bugzilla.mozilla.org/show_bug.cgi?id=914579)
* [Add support for Bonjour (Rendezvous/zeroconfig) to browser](https://bugzilla.mozilla.org/show_bug.cgi?id=173804)

From IPFS land
* https://github.com/ipfs/specs
* https://github.com/neocities/hshca

## Good Explanations

* [How /webui works](https://github.com/ipfs-shipyard/ipfs-companion/issues/718#issuecomment-490257566)
* [What "pinning" means, in detail](https://github.com/ipfs/integration-mini-projects/issues/4#issuecomment-490165343) 
* [On running IPFS on a laptop and moving between networks](https://github.com/ipfs/community/issues/408#issuecomment-490032167)
* [What makes something p2p (technical, still need a good non-technical)](https://github.com/qri-io/p2p-testbed#okay-so-what-makes-this-p2p)

## Privacy

* [How private is IPFS?](https://medium.com/pinata/ipfs-privacy-711f4b72b2ea) - good overview, Apr 5 2019, from Matt Ober @ Piñata
* [P2P privacy research papers](https://github.com/gpestana/p2psec/tree/master/research) - notes from Gonçalo Pestana

Implementations
* https://github.com/hashmatter/p3lib
* https://github.com/hashmatter/libp2p-onion-routing

HOWTOs
* [IPFS + I2P](https://medium.com/temporal-cloud/accessing-temporals-i2p-ipfs-infrastructure-7d9c90204dd7)
* [IPFS + Tor](https://github.com/flyingzumwalt/decentralized-web-primer/issues/38)

Content Moderation
* (see also that section in this document)
* [Infra blocklist](https://github.com/ipfs/infra/blob/master/ipfs/gateway/denylist.conf)

Conversations
* https://discuss.ipfs.io/t/is-it-possible-to-store-private-objects-in-ipfs-without-encrypting-them/460
* https://www.researchgate.net/publication/320853144_IoT_data_privacy_via_blockchains_and_IPFS
* https://www.reddit.com/r/ipfs/comments/9puvpo/question_about_ipfs_and_privacyright_to_be/

## Metrics/Telemetry/Analytics

* https://github.com/ipfs-shipyard/ipfs-webui/issues/980
* https://github.com/ipfs/ipfs-cluster/issues/721
* https://github.com/ipfs-shipyard/ipfs-webui/pull/930
* https://github.com/ipfs-shipyard/ipfs-webui/pull/985
* https://github.com/ipfs/awesome-ipfs/issues/200



## Design Questions

Visualizing hashes
* [on awesomeipfs](https://github.com/ipfs/awesome-ipfs/issues/176)
* Github as example for hash-based visual display that never shows a hash

Patryk work
* [Creating simple websites](https://github.com/ipfs/ipfs-gui/issues/69)
* [File browser](https://github.com/ipfs/ipfs-gui/issues/9)
* [Video player](https://github.com/ipfs-shipyard/ipfs-webui/issues/920)
* [Hash input context](https://twitter.com/patrykadas/status/1056288843035488257)
* [the Future of Browser History](https://medium.com/free-code-camp/browserhistory-2abad38022b1)

Captchas
* https://idena.io/?view=flip_challenge

Prior IPFS design work
* https://github.com/ipfs/user-research
* the docs personas
* mhz's murally

## Design Guidelines for Web Browsers

In preparation for browser integrations of IPFS and standardization efforts, we need a set of guidelines and recommendations.

This material will guide the smaller and experimental browser implementations, where we can learn and grow our experience in shipping IPFS.
It will set the context for larger browser vendors and standards bodies, providing a tangible proposal for discussion - letting us control the narrative instead of it being driven by their risk-averseness.

I've had a periodic meetup with some of the design team to get their input on some of the design bits needed to build our case with browser vendors.

## Addressing

* https://github.com/ipfs/in-web-browsers/blob/master/ADDRESSING.md
* [Irakli's note](https://www.notion.so/Addressable-data-projections-01371f85d15747cc9dff27a6cb7292c0)

## Architecture diagrams

Want (TODO: linkme)

* spectrum of threat model vs configurations of IPFS
* variations for the component, and interactions between them
* stack
* network view
* dht
* browser integration permutations
* how dapps use blockchains+ipfs

Code arch
* raw: https://raw.githubusercontent.com/ipfs/js-ipfs/master/img/architecture.png
* annotated: https://user-images.githubusercontent.com/1211152/47606420-b6265780-da13-11e8-923b-b365a8534e0e.png

Existing work

* https://github.com/protocol/design-shop/issues/112
* https://github.com/protocol/design-shop/issues/132
* https://app.mural.co/t/protocollabs6957/m/protocollabs6957/1537221476917/c9ca4403fac4054cac765237f6a9bc2a7cebec98

## Network Information

* https://ipinfo.io/AS40680
* Anycast
* peer with Packet

## Talks, decks

Juan's slides:

- Public talks: http://talks.benet.ai/
- Private talks: https://drive.google.com/open?id=1MqOj6SVMQEUDdUWZU_XDD82UP8GMHc0H

## Standards participation

Groups

* W3C
  * [Community group proposal](https://github.com/arewedistributedyet/arewedistributedyet/issues/27)
	* https://github.com/w3c-dvcg/lds-ed25519-2018/issues/3
* IETF
* IAB
* IRTC HRPC
* https://irtf.org/icnrg
* IGF

Pre-requisites

* Libp2p use-cases
  * [AWDY issue](https://github.com/arewedistributedyet/arewedistributedyet/issues/22)
  * [submitted](https://github.com/w3c/webrtc-nv-use-cases/issues/15#issuecomment-500303446)

Activities

* feedback opportunities

## Browser Feature Process

* [Chrome's Project Fugu](https://developers.google.com/web/updates/capabilities)

## Dweb pitch examples

* https://publishing.graphitedocs.com/sites/graphite.id/public/2236c29c-39b9-4ff3-9b97-5a5e24cf0af9
* https://www.inkandswitch.com/local-first.html

## Deployment how-tos

* https://withblue.ink/2018/11/14/distributed-web-host-your-website-with-ipfs-clusters-cloudflare-and-devops.html
* https://github.com/AuHau/ipfs-publish

## Community

* https://www.meetup.com/pro/ipfs

## Community discussion

* [HN on 2019 roadmap](https://news.ycombinator.com/item?id=19647692)

## Workshops/activities

* https://github.com/ssbc/scuttlebutt-mars-workshop
* https://noffle.github.io/kappa-arch-workshop/build/01.html

## Browser vendor approach

Drive based on use-cases, make our voice heard in standards bodies, create an environment where the change we want is possible.

* decision making matrix for dweb use-cases
* articulate use-cases, and blockers
* identify issues and corresponding bugs across vendors
	* (contrast against use-cases)
* browser integration permutation map (pros and cons for each)

Theory of change

* Outcomes
	* Browsers can communicate directly between each other without intermediary/broker
	* Web network stack can load from and publish to swarms
* In order for that to be possible...
	* TODO: write out all the things that *might* need to happen in order for the outcomes to be true

Classify roles, and architectural permutations

* native node (internal)
* native protocol
* native node + web api abstraction
* ipns/dns/ens/etc
* companion
* desktop
* gateway
* extension

## In-browser Limitations

* [Satazor on IDM work](https://github.com/ipfs/js-ipfs/issues/2093)

## Brave

* https://github.com/brave/brave-browser/issues/819
* [Brave issue tracking IPFS install prompt](https://github.com/brave/brave-browser/issues/3045)
* https://github.com/brave/brave-core/pull/1988
* https://github.com/brave/brave-core/pull/2328


## Opera

* https://twitter.com/ensdomains/status/1102884419017297921?s=19
* https://medium.com/the-ethereum-name-service/how-opera-is-using-ens-to-decentralize-the-web-ens-integration-spotlight-a545f7825724

## Mozilla

* libdweb

## Chrome

* Web Packaging
* Chrome.sockets.*

https://twitter.com/cramforce/status/1118488042493186048

## ENS

* spec: https://eips.ethereum.org/EIPS/eip-1577
* issue: https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1577.md
* https://github.com/ipfs-shipyard/ipfs-companion/issues/678

## Transports

* https://github.com/libp2p/interface-transport
* https://github.com/ipfs/js-ipfs/issues/1088

## Mobile

* Dev fastpath
  * React Native
  * Textile
  * Geckoview + WebExtensions

* Performance and battery testing
  * Heuristics vs use-cases

## React Native

* https://blog.datproject.org/2019/04/14/getting-dat-to-work-in-new-environments/
* https://github.com/tradle/rn-nodeify

## Content Moderation

Issues
* https://github.com/ipfs/go-ipfs/issues/1070

Discussions
* https://www.reddit.com/r/ipfs/comments/3m351b/discussion_permanent_content_dmca_and_illegal/
* https://steemit.com/ipfs/@dantheman/how-can-i-configure-ipfs-to-block-unwanted-content

Govt
* https://en.wikipedia.org/wiki/Child_abuse_image_content_list

## Visual communication model

* what is the threat model
* what is happening
* how much of it
* visual elements in context of user actions

## Timelines

* Visualize long term adoption arcs

## Pinning/saving language and design

* Find the existing issues in repos
* GUI+WB language exercise: https://ethercalc.org/pfn2sr40qogi

## Multiple daemons problem

* one repo
* cannot have situation w/ multiple nodes, so many connections
* instance per tab
* only use http? or profiles per instance?
* or global instance in service worker, namespaced per domain
* jim pick: same website in multiple tabs - iframe
* Lunet
* if ip addresses are exposed, can local daemons detect each other and negotiate activity?

## Identity

* https://github.com/ipfs-shipyard/pm-idm

## Research

* [FAQs](https://docs.google.com/document/d/1FBB_jn1BmwUFdZGQZN93ofcDFFoKM_P_CgwbCfH-gwk/edit)

## Notes on business prop for large network/content providers

Open questions
* Tracking?
* Privacy?

Video delivery bandwidth reduction
* With video delivery, a P2P approach could save 60% in bandwidth costs
* http://math.oregonstate.edu/~kovchegy/web/papers/p2p-vdn.pdf
* Examples: D-Tube, PeerTube

Performance
* Highly localized distribution of network load
* Customers sharing w/ customers at router level
* User experience: Improved response time for popular content
* Network wide predictivity goes up, and noise goes down
* Fewer single points of failure
* Adaptive at peak times
* Examples: Infura, Piñata, Cloudflare

Risk mitigation
* Content addressing provides new tools for illicit material identification
* Location is transiet, content can be copied anywhere
* Block by hash instead of location.
* Location can change, but hashes are forever.
* Content addressing reduces the attack surface for security risks
* MITM, location spoofing, phishing
* Hand-waving commences, I'm riffing at this point

Future: Preparation for dynamic markets for excess capacity
* Filecoin pitch
* Bandwidth freed up?

Challenges
* QOS
* Privacy vs tracking

## Lisbon Hack'n'plan: Unixfs v2
 
have metadata in v1, but nothing uses
why?
pms can tarball
"oh yeah that'll be fixed in v2"
symlinks shows up on a reg basis
works fine
except gateway
permissions shows up
can wrap in tarball
modified time
need to know whne things change
will be chasing upstream source
wrapping rsync
compare vs localtime
is owner useful?
do ppl build on it?
yes, but is not reliable
pms do this
pacman, can set owner
unzipped, keeps owner
tl;dr: need it, 
but how to deliver
has partial spec
what's right way to do directories
what is std way to do x
data chunking work
ipfs uses hamps
filecoin has made improvements
keep rehashing until you get the right places
do gap analysis to see what's missing in oerder to ship v2?
in okr roadmap, seems already aware of what's missing
in go, reactoring interfaces to be ipld
filecoin really wants graphsync and selectors
selectors would be good perf impr?
easy if you know structure of the tree
ideally sels operate on shards
no req for selectors in v2
mfs
v2 allows us to store metadate more easily
somethings can't tell fuse
no idea what happened with file
which meant acted less like a rreal fs
can we take partial spec, wishlist, and do rough impl that makes it easier for pms?
nothing in spec about sharded dirs
better for someone not on ipld to do it
so they'll get it done faster
someone needs to work w/ hamps and champs
need someone on ipfs to pull on it
filecoing is pulling on selectors, etc
not sure if sharded dirs relevant to pms
any blockers?
after 1.0, can do new features but very rarely changes hashes
ACTION: what is higher priority that is needed in v2?
ipld team maybe doesn't find it important
but ipfs team knows it's important for pms
now can go back to ipld and state priority
need someone on ipfs to pull on it
otherwise flls into endless perfection loop
ACTION: this quarter, set someone up to pull

## Lisbon Hack'n'plan: Notes on Magicalness

ipfs drive
  rework file api
  multiple routes
  drive is easy to process
  make mfs per ipns key
  each time modify, publish to ipns
  sorta makes a pm tree seamless
  dedicated drive for pinned content
  with different guarantees
  eg now not guaranteed in your repository
  makes it easier to build good guis
  if you have these drives, you can do lots of things
  eg shared drive
  bidirectional sync like dropbox from this drive abstraction
  special purpose drives
  need a step that collapses all our files apis
  not intuitive/familiar, don't self explain
  ppl don't know about mfs, for example
  ipfs add, mfs, and now we have another abstraction?
  or replace all of them?
  now you have mfs, which would be default drive
  but with multiple roots
  ACTION: throw away the old api and make a new one
  IPFS-x
  people excitedc about refactoring whole api
  pinning is non-intuitive
  refs supports abuse of public gateways
  maybe outline all wishes and reqs
  have one wg move on this
  come back to core team with use-cases
  need to clean up all surface area
  timebox it, like 3 weeks eg
  need to do before ipfscamp
  because can't break after that
  how to communicate to users
  multi-homed mfs-s
  is that too soon?
  what does 1.0 look like?
  lots of feedback to reduce surface area
  ipns - pluggable but not part of main surface area
  more pluggable/modular
  integration points
  for experimentation
  and organizing codebase
  commands and subcommands? pipe-able to somewhere else
ipfs rsync
  speaks rsync protocol
  hard dep on unixfs? no idea
  useful for pms
  instead of ip/hostname
  sync to current location
  get fuse working and use rsync?
  rsync the clojure repo
  don't want mfs to be propagating up the chain?
  need something for mirrors and maintainers to easily run
  one command, takes care of it
  removed a lot of work
  on client side, still need transport (but can use gateways)
  other path: filestore
  also one command
  what does filestore mean
  blockstores vs mfs vs filestore
  also urlstore
  filestore, gets path on local system
  and as long as you don't change the paths
  needs 2x the disc, 36 hours the first time
  redefine the okr?
  four different ways to do it
  just need to be able to say this is how to do it
  already written up in pm repo
  ACTION: write blog post
  there is no spec for rsync
  call to action for all the system pkg managers
  here's what's changed, time to change again
wasm
  can we have some?
  go rust way, use some crate and have wasm module
  or assembly script - typescript w/ std library, modeled to work well w/ wasm
  the output is clean and small
  instead of just bindgen, need more tools
  to remove stuff from actual wasm module
  hard, but getting better
  requires more getting into rust
  using assemblyscript, but need to write the code
  or, rather than wasm, are there other things that'd benefit from wasm?
  can use same wasm module everywhere
  perf
  protocol buffers, cbor, hash functions
  crypto apis
  would require some community effort?
  less problem with transpilation edge cases
  downstream packeges binaries for diff platforms
  wasm has no io, etc
  not a silver bullet
  chunking algorithm
alternative envs
  react native, electron, mobile
  doesn't work in electron right now
  node.js mobile
  iwb on mobile
  running for an app
  can we have a build that allows more experimentation
  probs like libp2p doesn't re-establish connections
  no perf profiles in js ipfs
  need a way of not opening a million connections
  actual size of bundles
  vue
  commonjs vs esmodules
  webpack bundling issues
  .default to requires, etc
  theoretically small things, but win whole communities
  top to bottom vs other way round
  similar to pm strategy
  how to create demand vs selling risks
  documenting package managers domain problems - that ipfs has solutions for
  can you replicate to other space? like photo sharing?
  hone the approach to applying to new problem spaces
ipfs archives
  build a community around public datasets
  where to find datasets
  how to offer space
  what's the flow/experience?
  will show how there's a large community of contributors willing to provide the service
  similar to tor exit node volunteering
  how many replicators? you can be one
  also tests ability to replicate these
  data hoarder subreddit
  people excited + prove the technology
  pms - have solved bandwidth - b/c fastly and cloudflare
  not incentivized to shift
  but have no people or eyeballs
  illusion of no people involved when you do npm install
  code as infrastructure
  eg impl features or security
  that's where pms are feeling the pain
  cared more sometimes by users than maintainers
  why are they excited about using ipfs?
  security, trust
  didn't have a crowbar to force it
  nobody doing chain of trust
  language pms not doing this
  but system pms do care about reproducibility
  verifiability
  then build reputation on top


* What are the recurring events?
* 


## JS

* https://www.reddit.com/r/javascript/comments/d5vn9f/research_shows_that_global_demand_for_javascript/
* lang populations: https://www.reddit.com/r/javascript/comments/bh6ill/javascript_is_and_remains_the_queen_of/

## Misc data

* internet live stats
* GlobalWebIndex
* https://blogs.loc.gov/thesignal/2011/11/the-average-lifespan-of-a-webpage/
* https://www.theatlantic.com/technology/archive/2015/09/how-many-websites-are-there/408151/
* [PWA Stats](https://www.pwastats.com/)

* [HN on Dropbox, 2007](https://news.ycombinator.com/item?id=8863)

Numbers
* https://www.reddit.com/r/dataisbeautiful/comments/dvx7ph/oc_how_50k_look_vs_1_million_vs_1_billion/
* https://www.reddit.com/r/dataisbeautiful/comments/dvli0r/oc_my_attempt_to_demonstrate_the_difference/

## IPFS Wins

* https://www.sciencealert.com/the-sum-of-three-cubes-problem-has-been-solved-for-42

## C and C++ Implementations

* [Discussion on ipfs/notes](https://github.com/ipfs/notes/issues/355)


* [libp2p in C++, Soramitsu](https://github.com/soramitsu/libp2p)
* [IPFS HTTP API client in C++](https://github.com/vasild/cpp-ipfs-http-client)
* [IPFS in C, Agorise](https://github.com/Agorise/c-ipfs)


## W3C

Activity related to PL
* [AWDY issue suggesting a CG](https://github.com/arewedistributedyet/arewedistributedyet/issues/27)
* [webrtc-nv-use-cases](https://github.com/w3c/webrtc-nv-use-cases/issues/15)
* [Digital Verification CG - Use of Multibase, Multicodec, and Multihash](https://github.com/w3c-dvcg/lds-ed25519-2018/issues/3)

W3C Strategy
* [Funnel](https://github.com/w3c/strategy/projects/2)

Joining
* https://www.w3.org/Consortium/join
* https://www.w3.org/Consortium/membership-faq
* https://www.w3.org/Consortium/fees?countryCode=US&quarter=01-01&year=2020#results

Community Groups (general)
* [w3c cg activity dashboard](https://w3c.github.io/cg-monitor/)

Possibly Relevant CGs
* [Blockchain](https://www.w3.org/community/blockchain/)
* [Solid](https://www.w3.org/community/solid/)
* [HTTPS in Local Network](https://www.w3.org/community/httpslocal/)
* [Bitcoin Hypermedia](https://www.w3.org/community/bitcoin/)
* [Unhosted](https://www.w3.org/community/unhosted/)
* [Blockchain Digital Assets](https://www.w3.org/community/digital-asset/)
* [Blockchain and Decentralized Apps](https://www.w3.org/community/dapps/)
* [Smart Contracts](https://www.w3.org/community/smartcontracts/)
* [Locations and Addresses](https://www.w3.org/community/locadd/)
* [Decentralized Communications](https://www.w3.org/community/decentralizdcomm/)
* [Web Archivability](https://www.w3.org/community/webarchivability/)
* [Decentralized Sharing](https://www.w3.org/community/decsharing/)
* [Distributed User Interfaces](https://www.w3.org/community/dui/)
* [Digital Verification](https://w3c-dvcg.github.io) - considering multibase/hash/codec
* [Object RTC](https://www.w3.org/community/ortc/) - doing QUIC P2P work

P2P
* [P2P and the W3C (2001)](https://www.w3.org/2001/04/w3c-p2p/Overview.html), fascinating preview of where IPFS and blockchains eventually end up
* [Early press re WebRTC's P2P vision (2011)](https://www.zdnet.com/article/w3c-to-develop-peer-to-peer-browser-standards/)

QUIC and P2P
* https://w3c.github.io/webrtc-quic/

## WebRTC

* [A Study of WebRTC Security](https://webrtc-security.github.io/)

TCP/UDP/Ports
* [WebRTC when only TCP port 80 and 443 are open, and all UDP blocked](https://groups.google.com/forum/#!topic/discuss-webrtc/bq2tUi_guE4)
* [Port requirements](https://groups.google.com/forum/#!topic/discuss-webrtc/PTPDF4D8m2A)
* [High Performance Browser Networking - WebRTC chapter](https://hpbn.co/webrtc/)
* [Intro to WebRTC's NAT problem wrt P2P](https://webrtchacks.com/an-intro-to-webrtcs-natfirewall-problem/)

QUIC
* [Who needs Quick in WebRTC anyway?](https://bloggeek.me/who-needs-quic-in-webrtc/)
* [QUIC for P2P - w3c cg report](https://w3c.github.io/webrtc-quic/)
