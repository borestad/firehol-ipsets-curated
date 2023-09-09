# firehol-ipsets-curated

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/borestad/firehol-ipsets-curated/ci.yml?style=for-the-badge)
![GitHub Workflow Status](https://counterapi.com/counter.svg?ns=codeit.se&action=view&key=cronboilerplate&style=big&startNumber=1&color=blue)
![GitHub repo size](https://img.shields.io/github/repo-size/borestad/firehol-ipsets-curated?style=for-the-badge)
![LICENSE](https://static.codeit.se/badges/mit.svg?repo=firehol-ipsets-curated)

**Motivation**

Since [firehol/blocklist-ipsets](https://github.com/firehol/blocklist-ipsets)
seems
[unmaintained](https://github.com/firehol/blocklist-ipsets/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc) -
there's a number of issues with not-so-updated blocklists. This is an attempt to
reuse as much as possible of the fantastic firehol with as little maintainence
as possible

### Disclaimer #1

- Do not use blocklists blindly on `OUTGOING (DST) <=> LAN/WAN`
- Do not use blocklists blindly on `OUTGOING (DST) <=> LAN/WAN`
- Do not use blocklists blindly on `OUTGOING (DST) <=> LAN/WAN`
- ...
- This automatically solves issues like
  [this](https://github.com/firehol/blocklist-ipsets/issues/265) or
  [this](https://github.com/firehol/blocklist-ipsets/issues/268) or
  [this](https://github.com/firehol/blocklist-ipsets/issues/243)

### Disclaimer #2

- Rules are supposed to be applied on `INCOMING (SRC) => WAN`
- Use a DNS-blocker if you want to block outgoing traffic instead of ips.
- If you block `OUTGOING (DST) => WAN/LAN` - you **WILL have trouble** when
  false positives mistakenly slips through. _Shit happens_ ¯\ _ (ツ) _ /¯
- If you find any false-positives, please contact the maintainer of the actual
  blocklist.
- All credits goes to [firehol](https://firehol.org) and all the maintainers of
  blocklists.

### Differences

- This repo is for _my_ private purpose.
- Automatic removal of ipranges from _legitimate_ sources like github.
- Automatic removal of
  [private ipranges](https://www.rfc-editor.org/rfc/rfc1918) (this is a job for
  the router instead)
- Removal of unused blocklists
- Removal of non maintained blocklists
- Only reuse the most common lists with as few false-positive as possible.
