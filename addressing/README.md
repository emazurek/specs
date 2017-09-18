# Addressing content on the distributed web

> Technical Report, Protocol Labs, August 2017

Location-based addressing is a centralizing vector on the web.
It lets links rot and drives copies of content into a mode of mutual competition.

We'll present a content-based addressing model for distributed networks,
which provides permanent links that don't rot and are cryptographically verifiable.
In this model, additional copies of content aren't hidden behind the original copy -
instead they foster cooperation and make for a more resilient and performant network.

- Introduction
- Namespaces
  - /ipfs
  - /ipns
  - /ipld
  - Other namespaces
- URL schemes
- dweb: URI scheme
- Web browser considerations


## Introduction

the rift web (uri) vs. os (fs)
- plan9 everything-is-a-file is nice
- fuse is nice
- ipfs aims to reunite fs and web

plan9
  https://news.ycombinator.com/item?id=3537259
  https://hn.algolia.com/?query=plan9&sort=byPopularity&prefix&page=0&dateRange=all&type=story

if we had URIs instead of multiaddr
p2p+tcp://bootstrap.libp2p.io/QmFoo
1. it doesn't fit the resource-on-server model
2. there's too many protocol combinations to have one URI scheme for each
church of context vs. church of self-description


## Namespaces

### /ipfs

### /ipns

### /ipld

### Other namespaces

Historic namespaces: /dns

/git /eth /btc /torrent

want to collaborate with all groups working on content-addressed stuff


## URL schemes


## dweb: URI scheme

We're not trying to bring in all the possible sources of data, or interfaces, etc.
We only work on content-addressed stuff here. But we do think paths are the better canonical address


## Web browser considerations

Security Model
Pluggable origins? would make this a bit easier. suborigins step in right direction

How to detect and intercept http-to-ipfs URLs in documents
- $hash.ipfs.somedomain ?
- could have links in document to //QmFoo.ipfs.link (http://) and //QmFoo (ipfs://)
