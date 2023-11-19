# Garden Fence

This blocklist is intended as a simple starting point for Mastodon server admins who want to protect their users from the worst and most well known sources of:

- Hate speech, racism, sexism, homophobia, transphobia
- Harassment, trolling, doxxing, stalking
- Alt-right, nazism, fascism
- Free-speech-as-in-bigotry, "just asking questions"
- Misinformation, anti-vax, conspiracy theories
- Sexualization of minors, potential for [CSAM](https://www.missingkids.org/theissues/csam)
- Spamming, denial-of-service, network disruption, abusive bots

## The Blocklist

**Last Updated**: 2023-11-19  
**Block Count**: 136  

### Downloadable Files for Import
- [gardenfence-mastodon.csv](https://github.com/gardenfence/blocklist/blob/main/gardenfence-mastodon.csv) (Mastodon format)
- [gardenfence-fediblocksync.csv](https://github.com/gardenfence/blocklist/blob/main/gardenfence-fediblocksync.csv) (fediblock-sync format)

**Mastodon**
: As of version 4.1, blocklist files can be imported and exported from the admin interface, under **Moderation > Federation**.

**fediblock-sync**
: The comand line tool **fediblock-sync** available from [fediblockhole](https://github.com/eigenmagic/fediblockhole) can be used to import blocklists from multiple sources, including remote servers, URLs, or local files.

## How is the list created?

The Garden Fence blocklist is generated with a python script:

- Block lists are fetched from each of the reference servers
- *Suspend* level blocks are counted, *Limit/Silence* blocks are ignored
- Blocks of subdomains count towards the root domain (blocking `social.bad.example` is counted as blocking `bad.example`)
- Suspensions which are shared by **at least 6 of the 7 of reference servers** are included in the list (~85%)
- Tags are added by matching against the comments provided by the reference servers
- Servers which are believed to be offline are filtered out to reduce clutter

### Reference Servers

The admins of these servers have given permission for their block lists to be used for the purpose of generating this combined blocklist:

- [sunny.garden](https://sunny.garden)
- [mastodon.art](https://mastodon.art)
- [mastodon.social](https://mastodon.social)
- [rage.love](https://rage.love)
- [toot.wales](https://toot.wales)
- [tenforward.social](https://tenforward.social)
- [solarpunk.moe](https://solarpunk.moe)

The admins of these servers make their own determinations about which servers to block, and represent a variety of administrative styles and approaches to evaluating the importance of blocking any particular server. They do not necessarily endorse the entire content of the final blocklist, or suspensions made by other servers.

## What this list is *not*...

### Neutral / Unbiased

This is not a neutral or unbiased survey of which servers are most blocked across the fediverse. It is highly biased against the various forms of unwanted content mentioned above.

### Comprehensive

This list contains only the most blocked servers among the selected group of reference servers.  Some of these servers on their own have much longer blocklists, and there are surely other servers that you may wish to block that are not listed.

It also does not necessarily represent all of the different kinds of content that you might want to block depending on the goals and values of your particular server, such as porn, crypto, bots, etc.

It is also highly biased towards English content, and may not provide good coverage for content in other languages.

### Realtime

Updates are typically processed and reviewed once a week.

# Other Blocklists

One of the aims of the Garden Fence blocklist is simplicity. There is only one list, it can be used for manual or automatic import, and I aim to keep it as straightforward as I can.  

It might not suit your needs though.  These are some other lists which you might find useful:

- [Seirdy's Fediverse Blocklists](https://seirdy.one/posts/2023/05/02/fediverse-blocklists/) has several manually curated block lists in different levels of severity.

- [Oliphant’s Blocklists](https://writer.oliphant.social/oliphant/blocklists) contains a variety of lists automatically combined from several reference sources.
