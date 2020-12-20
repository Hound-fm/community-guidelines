# Metadata Standard

### Overview
| :warning: | Work in progress, we need more help and feedback from the community.
|---|:---|

### Metadata

> Metadata is structured information about a stream or channel separate from the content itself (e.g. the title, language, media type, etc.). It is stored in the blockchain as the value property of a claim.

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
|---|:---|:---|
| `license` | License identifier | Required

All Rights Reserved identifier:

> Copyright is automatically granted to you when you begin creating your work. You don't have to file anything anywhere, or publish anything online to own the copyright of your music. By choosing All Rights Reserved, you ask that other creators not use your material.  
https://help.soundcloud.com/hc/en-us/articles/115003566468-Choosing-a-license-for-your-track

Is recommended to use the `ARR` identifier or the legacy string `All Rights Reserved` instead a copyright notice unless otherwise required.

> US law no longer requires the use of a copyright notice, although placing it on a work does confer certain benefits to the copyright holder. Prior law did, however, require a notice, and the use of a notice is still relevant to the copyright status of older works. 


CC License identifier format:

```
- All identifiers should start with the creative commons 2-Letter abbreviation (CC)
- It must include all the license terms on a 2-Letter abbreviation (BY, NC, SA etc..) separated by a hypen (-)
- License version should be provided at the end on semantic versioning format ( 3.0, 4.0, etc..) 
```

```
License name: Attribution-NonCommercial-ShareAlike 4.0 International
License identifier: CC BY-NC-SA 4.0
```

For public domain is recommended to use `CC0` as the identifier instead of the legacy string `Public domain`.

Example:

```
License name: CC0 1.0 Universal (CC0 1.0) Public Domain Dedication
License identifier: CCO
```

Why use an identifier and not the license name ?

Identifiers are short strings so they can take less space and are easy to process by other software or programs.
They also help dealing with multilingual content, for example take a look at this two licenses:

> Attribution-NonCommercial-ShareAlike 4.0 International
> Attribution - Pas d’Utilisation Commerciale - Partage dans les Mêmes Conditions 4.0 International
> Attribution - Pas d’Utilisation Commerciale - Partage dans les Mêmes Conditions 4.0 International

Unless you can read and understand both languages (english, french) it is difficult to tell if they are the same license or different types.

Please see for a full list of identifiers: https://creativecommons.org/licenses/
 
#### Missing fields:

> The P Line, often marked with a ℗, identifies that their is an owner to the rights of a sound recording. Whatever follows the P Line should identify who is the owner of those rights.

> The C Line, symbolised with a ©, is the copyright of the music but not the sound recording itself. The C Line signifies the copyright owner of the music but not recordings of it. 

For more information:
https://routenote.com/blog/what-do-the-p-line-and-c-line-mean-in-music-copyright/
https://artists.spotify.com/blog/talk-the-talk-music-terms-a-glossary
