# Garden Fence

This blocklist is intended as a simple starting point for Mastodon server admins who want to protect their users from the worst and most well known sources of:

- Hate speech, racism, sexism, homophobia, transphobia
- Harassment, trolling, doxxing, stalking
- Alt-right, nazism, fascism
- Free-speech-as-in-bigotry, "just asking questions"
- Misinformation, anti-vax, conspiracy theories
- Sexualization of minors, potential for [CSAM](https://www.missingkids.org/theissues/csam)
- Spamming, denial-of-service, network disruption, abusive bots

Follow [@gardenfence@sunny.garden](https://sunny.garden/@gardenfence) for notification of weekly updates or other important changes to the list.

## The Blocklist

**Last Updated**: 2026-01-04  
**Block Count**: 147  

### Downloadable Files for Import

**Before importing this or any blocklist, you are encouraged to spend some time reviewing its contents to ensure that it agrees with your values and criteria for the domains you wish to block. Keep in mind that viewing the content on some of the listed domains will expose you to hate speech, uncensored explicit imagery, or worse... Proceed accordingly.**

- [gardenfence-mastodon.csv](https://github.com/gardenfence/blocklist/blob/main/gardenfence-mastodon.csv) (Mastodon format)
- [gardenfence-fediblocksync.csv](https://github.com/gardenfence/blocklist/blob/main/gardenfence-fediblocksync.csv) (fediblock-sync format)

**Mastodon**
: As of version 4.1, blocklist files can be imported and exported from the admin interface, under **Moderation > Federation**.

**fediblock-sync**
: The command line tool **fediblock-sync** available from [fediblockhole](https://github.com/eigenmagic/fediblockhole) can be used to import blocklists from multiple sources, including remote servers, URLs, or local files.

## How is the list created?

*As of Sep. 2024, only domains which are blocked by sunny.garden are included in the list.  In practice, this has been the case since Nov. 2023, but it is now enforced as a requirement.*

- Domain is blocked by sunny.garden
- Domain is also blocked by a minimum number of additional reference servers (subject to change, but currently 6 out of 7).
- *Suspend* level blocks are counted, *Limit/Silence* blocks are ignored
- Blocks of subdomains count towards the root domain (blocking `social.bad.example` is counted as blocking `bad.example`)
- All additions and removals from the list are manually reviewed.

Tags are added by matching against the comments provided by the reference servers.

Domains may be excluded from the list if they are believed to be offline, or if the reason for the block is outside the intended scope of the blocklist, even if they are widely blocked (eg. threads.net, or bridges to twitter/bluesky/mostr).

### Reference Servers

As of Sep. 2024, servers used as references for filtering are no longer listed. This is primarily due to the time and effort required to find suitable reference servers that are *also* willing to be publicly listed as such, making it extremely difficult and time consuming to replace any server that is no longer being used as a reference.

A related change, as noted above, is that the blocks from reference servers are now used to filter down the sunny.garden blocklist to include the most widely blocked "worst of the worst" domains.

Reference servers are selected which have compatible values, operate relatively independently of each other, and are known to actively monitor and block problematic domains. 

## What this list is *not*...

### Neutral / Unbiased

This is not a neutral or unbiased survey of which domains are most blocked across the fediverse.  The contents are based on the judgements made building sunny.garden's blocklist, and filtered down using other servers as references to help determine relevance to other servers with compatible values.

Judgement is used during manual review when compiling the resulting list before publishing.

### Comprehensive

This list contains only domains blocked by sunny.garden which are also blocked by a majority of reference servers.  There are surely other domains that you may wish to block that are not listed.

It also does not necessarily represent all of the different kinds of content that you might want to block depending on the goals and values of your particular server, such as porn, crypto, bots, bridges, etc.

It is focused on English content, and will likely not provide good coverage for content in other languages.

### Realtime

Updates are typically processed and reviewed once a week.

# Other Blocklists

One of the aims of the Garden Fence blocklist is simplicity. There is only one list, it can be used for manual or automatic import, and I aim to keep it as straightforward as I can.  

It might not suit your needs though.  These are some other lists which you might find useful:

- [Seirdy's Fediverse Blocklists](https://seirdy.one/posts/2023/05/02/fediverse-blocklists/) has several manually curated block lists in different levels of severity.
- [Awesome Fedi Admin Resources](https://codeberg.org/nev/awesome-fediadmin/#basic-blocklists) has a list of Basic Blocklists in addition to other other resources for fedi admins.