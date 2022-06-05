# Obsidian Flip Cards (WIP)

Obsidian Flip Cards is a snippet created for the Obsidian note taking app, that turns markdown tables into flip cards as shown in the images below.

...

...

## Installation

To install this snippet, simply download **flip-cards.css** and place it into Obsidians **snippet** folder.

## Usage

To use the snippet within your files, add the following YAML to the top of your file:

```yaml
---
cssClasses: cards
---
```

In addition, for the cards to display correctly, the first column of the table **HAS** to be the image. It is recommended that the 2nd column be used for the title as it is specifically styled to be used for titles.

```markdown
|            Cover Image           |        Title       | ... | ... |
| -------------------------------- | ------------------ | --- | --- |
| ![[image.png]] OR ![](image.png) | [[Title]] or Title | ... | ... |
```

The same has to apply for dataview tables. Below is an example of how such a dataview table might look like.

```dataview
TABLE WITHOUT ID
    cover AS "Cover",
    "[[" + file.name + "]]" AS "Title"
    ... AS "...",
    ... AS "..."
 FROM ...
 SORT ...
```

## Recommended Plugins

Plugin | Use
-- | --
**Sortable** | Necessary to make tables sortable.
**Advanced Tables** | Makes working with tables easier and faster.
**Dataview** | Necessary to create dataview tables which come with filtering options.

## Compatibility

Due to each obsidian theme having it's own styling, some parts of the flip cards may break. Below is a list of theme's for which I have checked and adjusted the code so that it "shouldn't" break.

- Obsidian Base Theme
- Minimal
- Blue Topaz (limited)
- Things
- Yin and Yang
- Atom
- Deep Work
- California Coast

## Additional Features

The snippet comes with a bunch of additional features that can be toggled by adding certain keywords to the YAML.

### Page Width

### Columns

### Aspect Ratio

---

This is a css snippet for the Obsidian note-taking app that turns regular markdown tables into card-based tables. 

It's heavily inspired by [Minimal Theme's](https://github.com/kepano/obsidian-minimal) card view.

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

## Future plans:
- [x] Add support for dark mode.
- [ ] **Maybe:** Use Style Settings to add some customization options. (Font size, color, spacing etc.)
- [x] **Maybe:** Alternate Styles for the cards
- [ ] When hovering over a card that is only half shown, the screen shackes when the flip happens. Need to look at what causes this to happen and fix it. Only happens if the card in question has an iamge, so I assume it has something to do with the iamge. Maybe it being hidden when flipped or something.
