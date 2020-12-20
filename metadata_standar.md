# Metadata Standard

### Overview
| :warning: | Work in progress, we need more help and feedback from the community.
|---|:---|

### Metadata

> Metadata is structured information about a stream or channel separate from the content itself (e.g. the title, language, media type, etc.).
> It is stored in the blockchain as the value property of a claim.

| :information_source: | The content of this document will cover only specific areas for improvement, please read the complete metadata [specification](https://lbry.tech/spec#metadata)
|---|:---|

### Open Standard

> Using standardised metadata descriptions makes datasets:

    - More discoverable
    - Easily syndicated
    - Transferable
    - Easily combined with other datasets
    
> Ultimately makes it easier for datasets to be used in real-world situations to add value.

Source: [Metadata standards for open data](https://salsadigital.com.au/insights/metadata-standards-for-open-data)

| :warning: | Work in progress, we need more help and feedback from the community.
|---|:---|

### Licensed content

Copyright is a law that gives the owner of a work (for example, a book, movie, picture, song or website) the right to say how other people can use it. These rights include:

```
- The right to reproduce the work.
- Prepare derivative works. 
- Distribute copies. 
- Perform and display the work publicly.
```
 It helps protect authors from other people copying their works without permission and/or for commercial purposes.
 
 Including this information on the metadata is important to prevent unintentional copyright infringement and makes easy for everyone to discover, share, reuse or remix content legally.
 
 #### Metadata fields: 
 
| Name | Description | Required
|---| :---| :---
| `license` | A valid spdx license identifier or english acronym | Required
| `license_url` | A valid url for the actual license | Not required

#####  Why use an identifier and not the license name ?

Identifiers are short strings so they can take less space and are easy to process by other software or programs.

By providing a short identifier, users can efficiently refer to a license without having to redundantly reproduce the full license. 

They also help dealing with typos and multilingual content, for example take a look at this two licenses:

```
- Attribution-NonCommercial-ShareAlike 4.0 International
- Attribution - Pas d’Utilisation Commerciale - Partage dans les Mêmes Conditions 4.0 International
```

Unless you can read and understand both languages (english and french) it is difficult to tell if they are the same license or different types.

Example using the correct format:

```JSON
{ "license": "CC-BY-NC-SA-4.0" }
```

Learn more: https://spdx.org/licenses/


#### All Rights Reserved identifier:

There is no identifier registered for "All rights reserved" on the SPDX License list, but you can use the `ARR` acronym instead of the legacy string. 

Example using the correct format:

```JSON
{ "license": "ARR" }
```

#### Public domain

For public domain is recommended to use the `CC0-1.0` spdx-license-identifier or the english acronym `PD` instead of the legacy string "Public domain".
 
Example using the correct format:
 
 ```JSON
{ "license": "CC0-1.0" }
```
 
 #### License url
 
 With a valid spdx license identifier there is no need to provide an url and the `license_url` field can be ignored. However if your content is published under a different license that is not registered on the SPDX License list please include a valid one.
 
Example using the correct format:

```JSON
{ "license_url": "http://domain.com/custom_license/1.0/archive.txt" }
```

 <!-- TODO: Add Missing fields for P-LINE, C-LINE:

Find a way to extend metadata for the following fields

> The P Line, often marked with a ℗, identifies that their is an owner to the rights of a sound recording. Whatever follows the P Line should identify who is the owner of those rights.

> The C Line, symbolised with a ©, is the copyright of the music but not the sound recording itself. The C Line signifies the copyright owner of the music but not recordings of it. 

For more information:
https://routenote.com/blog/what-do-the-p-line-and-c-line-mean-in-music-copyright/
https://artists.spotify.com/blog/talk-the-talk-music-terms-a-glossary

-->

#### Legacy strings

Legacy strings are supported for compatibility with old metadata published and they will be deprecated in the future. You should use the english acronym instead.

| Name | Legacy string
|---| :---
| `PD` | Public Domain
| `ARR` | All rights reserved

### Extending the metadata

Some types of content require very specific metadata information wich is not provided in the current metadata schema.
Since most platforms interpret the `description` field as markdown, it is possible to include nested metadata within this field using yaml front matter:

> Front matter is metadata written in yaml, located at the top of a file wrapped in ---'s.

Front matter example:

``` YML
---
key: value
---

Additional content ( usually as markdown format )...
```

The nested metadata included on the yaml block should be very minimal and only used if the current metadata fileds don't provide enough information.

Nested metadata keys should follow a specific naming convention and the values should only include common data types such as string or numbers.

