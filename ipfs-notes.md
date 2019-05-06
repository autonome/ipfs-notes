# IPFS Notes

## Meta

* My Zoom URL: https://protocol.zoom.us/my/dietrich.pl
* My Calendly: https://calendly.com/dietrich-pl

## Activities

* Browsers
* Metrics
* Events
* IPFS Companion

## Playtime

* how to do time series data on ipfs? ipns -> cid -> pubsupdates
* IPFS PWA share target
* sketchlog
* React Native IPFS playground
* conversational interface
* Frame as IPFS-native browser, as registered handler for ipfs protocol
* Multipublish: static publish -> dat/ipfs/ssb/activitypub

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

## Web Standards & Browser Dependencies

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

Dapps
* [Add dweb.link to public suffix list](https://github.com/publicsuffix/list/pull/766)

mDNS and related
* [Add Network Service Discovery API support](https://bugzilla.mozilla.org/show_bug.cgi?id=914579)
* [Add support for Bonjour (Rendezvous/zeroconfig) to browser](https://bugzilla.mozilla.org/show_bug.cgi?id=173804)

## Metrics

* https://github.com/protocol/metrics
## Privacy

* [How private is IPFS?](https://medium.com/pinata/ipfs-privacy-711f4b72b2ea?sk=de4e4a95b19260bda95fe695e63099cd) - good overview, Apr 5 2019, from Matt Ober @ Piñata
* [P2P privacy research papers](https://github.com/gpestana/p2psec/tree/master/research) - notes from Gonçalo Pestana

* [Infra blocklist](https://github.com/ipfs/infra/blob/master/ipfs/gateway/denylist.conf)

## Slang

* IPFS
* IPLD
* IPNS
* libp2p
* protobuf
* UnixFS
* UnixFSv2
* CID
* CIDv1
* Multiformats
* Multicodec
* IPFS Companion
* IPFS Desktop
* DAG
* DHT
* Filecoin
* GraphSync
* GUI
* Merkle DAG
* Merkle tree
* MFS
* Block
* LabOS
* Circuit relays
  * https://github.com/ipfs/js-ipfs/tree/master/examples/circuit-relaying
  * https://github.com/ipfs/go-ipfs/blob/master/docs/experimental-features.md#circuit-relay
  * https://github.com/libp2p/specs/blob/master/3-requirements.md#35-relay
  * https://github.com/libp2p/specs/tree/master/relay
* Multihash
* Multicodec
* Blockstore
* Content routing
* DHT:
* DNSLink
* ENS
* IPFS
* IPLD
* IPNS
* Key
* Libp2p
* Multiaddr
* Multihash
* Namespace
* Peer
* Peer id
* SDP
  * https://tools.ietf.org/html/rfc4566
* Secio: ["What is Secio?"](https://github.com/libp2p/go-libp2p-secio/issues/7)
* Working groups

## Architecture diagrams

* variations for the component, and interactions between them
* stack
* network view
* dht
* browser integration permutations

## Standards participation

* membership
* wg
* tpac
* use-cases
* mailing lists
* feedback

## Browser vendor strategy

Drive based on use-cases

* decision making matrix for dweb use-cases
* articulate use-cases, and blockers
* issues and corresponding bugs across vendors
* (contrast against use-cases)
* browser integration permutation map (pros and cons for each)

Classify

* native node (internal)
* native protocol
* native node + web api abstraction
* ipns/dns
* companion
* desktop
* gateway
* extension

## Brave

* [Brave issue tracking IPFS install prompt](https://github.com/brave/brave-browser/issues/3045)

## Opera

* https://twitter.com/ensdomains/status/1102884419017297921?s=19

## Mozilla

* libdweb

## Chrome

* Web Packaging
* Chrome.sockets.*

## ENS

* https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1577.md
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

## Content Moderation

...

## Visual communication  model

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

