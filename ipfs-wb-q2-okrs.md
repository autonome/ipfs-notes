# IWB Q2 Hopes & Dreams (aka OKRs)

Included P3 and greater here in order to capture all surface area covered in planning sessions, but only moved P0/P1 to the planning sheet.

Rough criteria for P values that we used in planning sessions:

* P0: Do or die for the quarter
* P1: Designed for inclusion
* P2: Ongoing expected work (longer term / co-op)
* P3: Well, we got everything else finished, so...
* P4-999: Happy accidents, or future

P0 has been estimated, and falls within reasonable amount to accomplish within the time budget alloted in the Q2 OKRs planning document.

P2 describes things like browser vendor discussions or co-op work - escape hatch for "long-running processes" or cross-wg dependencies.

## Support IPFS Camp with Course Material
* P0: IPFS Camp: Core course on publishing websites on IPFS
* P0: IPFS Camp: Elective course on publishing websites on IPFS

### Course work notes (haha)

* Special cluster
* Template for share app
* Use Oli's stuff

## Support and accelerate Package Manager work

* P0: IPNS resolve time is less than 10 seconds in browser contexts
* P2: Built an IPFS-based Unpkg prototype

## Reduce surprises for web developers

* P0: JS-IPFS works in Vue-CLI projects 
* P0: JS-IPFS supports File and FileList
* P1: JS-IPFS can be included in ESM environments
* P2: CIDv1 Base32 is ready for use in subdomains with mutable content
* P2: JS-IPFS can be processed by Rollup
* P2: JS-IPFS has an IndexedDB-based datastore
* P2: JS-IPFS has a Universal API provider with configurable fallback heuristics
* P3: Bundle size has not regressed
* P3: Design and create a browser global ipfs instance based on Service Worker
* P4: JS-IPFS can be included in Parcel bundles
* P4: HTTP API/Gateway has interoperability tests
* P4: Lazy-loaded IPFS Proxy entrypoint is exposed to websites, the old API is removed 
* P4: Research and design IPFS provider for progressive peer-to-peer web applications (PPWA)

## Companion can support archiving of web content

*Background: This objective is a first take at reorienting strategy for Companion feature development around a set of use-cases for non-developer users in browsers.*

* P0: We've identified the primary use-cases for non-technical users, in order to drive strategy for Companion
* P2: User actions add content to MFS by default
* P2: Redesigned user experience for pinning (collab with GUI/Design WG)
* P3: User is able to save full snapshot of a website to IPFS

## Browsers are integrating IPFS and shipping it

* P0: We've defined what success is for native support in browsers, and have a long term strategy proposal for getting there
* P0: Brave: UI for new embedded node type exists in Companion
* P0: Brave: Companion uses embedded HTTP gateway (JS IPFS) by default
* P1: Brave: Embedded JS IPFS node is using P2P TCP based Transport
* P1: Brave: Embedded JS IPFS node performs mDNS-based Local Discovery
* P1: We've defined a strategy for standards body participation and influence
* P1: We've got a plan and roadmap with Opera
* P2: arewedistributedyet.com is collapsed to signposting (notes below)
* P3: HTTP Proxy mode is supported by JS IPFS and Companion (not blocking Brave, pushed b/c Go pushed)
* P3: We've hired an engineer to work on browser codebases

### UI for new node type
* Welcome screen text changes
* Button for starting/stopping local node
* UI for reflecting presence of advance features

## Support alternative environments

* P1: JS-IPFS can be bundled in Electron
* P2: JS-IPFS can be included and run in a React Native project

## Notes: Companion use-cases for non-technical users

* Archiving
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

## Notes: Add to backlog

* pinning / saving ux and language
* package manager (i know this hash!)
* what decentraleyes does

## Notes: AWDY

* high value collaborators use it
* but been some quarters since updated
* gets regularly deprioritized
* website needs something to happen
* can collapse content to signposting, so doesn't appear abandoned?

