## Community Guidelines

### Overview

This is the first version of our Community Guidelines. Please read carefully and don't forget to check for new updates.

| :warning: | Ignoring this guidelines doesn't benefit the community and it will result on a negative impact for discoverability and overall experience.
|---|:---|

#### Not Allowed

:x: Spam ( Fake accounts, unesessary curator actions, advertisment etc.. )

:x: Use or encourage metadata abuse ( See Content creators guidelines )

:x: Curate or publish unlicensed content ( Not having the official and legal permisions to publish specific content )

#### Summary

| :link: | Links
|---|:--- |
 :information_source: | [Overview](#user-content-community-guidelines)
| :information_source: | [Human curators](#user-content-human-curators)
| :information_source: | [Discover system](#user-content-discover-system)
| :information_source: | [Content creators](#user-content-content-creators)

## Human curators

Curators are people that help us [discover](#user-content-discover-system) new content published on lbry.
Everyone can become a curator by creating a [channel](https://lbry.tech/spec#channels) and following this guidelines:

- Discover and recommend awesome channels with original content.

- Report [unlicensed content](https://lbry.com/faq/dmca) or [metadata abuse](https://lbry.com/dmca)

- Verify metadata of new discovered content and notify creators if further changes are required to improve discoverability.

| :warning: | Only use a single channel for curation. It is recommended to include the `curator` tag in the channel metadata. ( This will be required in the future )
|---|:---|

## Discover system

Hound.fm provides a community-driven discovery system powered by [curators](...).

A "discover" is a simple action triggered by the curator on a new content, the first curator to trigger this action is assigned as the discoverer.

| :warning: | This actions should be triggered `only` on content that the curator wants to recommend to the community, in order to preserve a more organic discoverability.
|---|:---|

In other words a "discover" is basically a recommendation done by the curator and broadcasted to the community:

> Curator: Hey, I found this awesome track (stream claim) by `@channel`, check it out. 
>
> Hound.fm: Curator has discovered a new track by @channel, check it out.
> 
> Community: Ok nice, I'll listen later...

#### Curator actions:

An "action" is just an special [transaction](https://lbry.com/faq/transaction-types), once is verified it will take a few minutes to appear as a new discover.

| Name | Description
|---|:---|
| Repost | Share a link to another LBRY claim 

Only repost transactions are detected, but in the future we will include other types like supports, tips, reaction, ...etc.


Once the discover is verified it will be aggregated and broadcasted to the community.

| :warning: | It is important that the curator verifies the credibility of the content origins and the metadata provided: If not enough metadata is provided the content won't be aggregated and the discover is ignored, this is also true if the aggregation system detects metadata abuse.
|---|:---|


## Content creators
Content creators can publish original content on a specific channel:

#### Types of channels:

Based on musicbrainz [schema](https://musicbrainz.org/doc/Artist)

| Type | Description
|---|:--- |
| Person | This indicates an individual person.
| Group |  This indicates a group of people that may or may not have a distinctive name.
| Podcast | This indicates a podcast series, usually features one or more recurring hosts engaged in a discussion about a particular topic or current event.
| Publisher | Record labels, music publishers, or the company that owns it.

Different types of channels allows to have a clear `relation` between them:

- A `Person` can be linked as the host or guest of a `podcast`.

- Different members of a band can be linked to a `group`.

A discover with a relation of linked channels benefits all of them and not just the original publisher, and they can be consider as collaborators.

All programs and users publishing content should follow the open metadata [standard](https://github.com/Hound-fm/metadata-standard)

| :warning: | Work in progress, we need more feedback from other creators.
|---|:---|

