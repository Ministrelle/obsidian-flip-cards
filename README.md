# obsidian-table-cards (WIP)
This is a css snippet for the Obsidian note-taking app that turns regular markdown tables into card-based tables. 

It's heavily inspired by [Minimal Theme's](https://github.com/kepano/obsidian-minimal) card view.

**WIP:** This is still very much a work in progress. While the main part works well, there are still a lot of quality of life features missing, for example support for darkmode.

![Screenshot](https://github.com/Ministrelle/obsidian-table-cards/blob/f50dcd4fe3ad0ad5cd7e649c23ecfd3f12905353/card-view-screenshot.png)

![Screenshot-2](https://github.com/Ministrelle/obsidian-table-cards/blob/bae5cbd3263d902ec41750f45ea5a6dcd6a4a484/card-view-screenshot-2%20(2).png)

## How to use this snippet?

To use this snippet, download `card-tables.css` and put it into your vaults snippet folder.

Then add the following YAML to the top of your Obsidian file in which you want to activate the card-table:

```yaml
---
cssClasses: card-table
---
```

You can then change some aspects of the cards, as described below, by applying additional cssClasses to the document. e.g:

```yaml
---
cssClasses: card-table, columns-6, contain, aspect-16-9
---
```

## Recommended Plugins

Plugin | Use
-- | --
**Sortable** | Allows you to sort tables
**Contextual Typography** | Probably not needed, but not having it might break some things ... need to check \\(-_-)/

## YAML cssClasses

The snippet offers the following YAML cssCLasses to change certain aspects of the snippet:

### Aspect ratios

By default, the images are displayed at a `3:4` aspect ratio.

You can use the following cssClasses to change the aspect ratio to your liking:

cssClass | Effect
-- | --
`aspect-16-9` | Changes the images aspect ratio to 16:9
`aspect-1-1` | Changes the images aspect ratio to 1:1
`aspect-2-1` | Changes the images aspect ratio to 2:1
`aspect-2-3` | Changes the images aspect ratio to 2:3

### Columns

By default, the snippet decides the amount of columns by itself based on content size.

If you want to have a specific number of columns, you can use the following cssClasses:

cssClass | Effect
-- | --
`column-1` | Displays cards in only 1 column.
`column-2` | Displays cards in only 2 column.
`column-3` | Displays cards in only 3 column.
`column-4` | Displays cards in only 4 column.
`column-5` | Displays cards in only 5 column.
`column-6` | Displays cards in only 6 column.
`column-7` | Displays cards in only 7 column.
`column-8` | Displays cards in only 8 column.

### Image fit

By default, the iamges are set to cover, which means that they will fill out the available space without resizing. This can lead to parts of the image being cut off if the aspect ratios are too far off.

If you want to always show the entire image, no matter the aspect ratio, you can use the following cssClass to do that.

cssClass | Effect
-- | --
`contain` | Changes the image fit from **cover** to **contain**
