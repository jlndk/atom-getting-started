# Atom Getting Started

Guiden er lavet så det vigtigste står øverst :).

(Welcome screen kan slås fra ved at unchecke "Show welcome guide when opening Atom")

## SETTINGS (kan tilgås ved ctrl + ,)

### EDITOR
* font family (Kan anbefale Fira Code, men det er selfølgelig personlig preference)
* font size
* line height (1.45 bruger jeg)
* scroll past end (hvis du vil kunne rulle længere ned i filen end der er linjer)
* tap length: 4
* Tap type: soft/hard tabs (Soft = spaces, Hard = Tabs)

### PAKKER
**Basics**
* Atom Beautify (Automatisk formatering af stort set alle filtyper)
* Docblockr (Bedre oprettelse af kommentare)
    * Slå "extend double slash" fra under package settings
* Pigment (viser farver direkte i editoren)
* Emmett (lader dig skrive html meget hurtigt)
* Minimap (Enhanced scrollbar)
  * **Optional ekstra plugins for minimap:**
    * minimap-git-diff
    * minimap-highlight-selected
    * minimap-pigments (kræver pigments)
    * minimap-find-and-replace (kræver pigments)

**Advanced:**
* language-[language] (Syntax highlighting for et givent sprog (f.eks language-sass))
* linter + linter-[language] (validering af et bestemt sprog (f.eks linter-javac))

### THEMES
Dette er selfølgelig en meget personlig ting, men jeg kan stadig komme med nogle anbefalinger:

**Dark themes:**
* Atom material + Base16 Tomorrow Dark
* Northern Dark + Northern Dark Atom

**Light themes:**
* Jeg er ikke en scrub, men hvis i har nogle gode light themes kan i bare oprette en PR

### CUSTOMIZATIONS:
#### Keymap (custom shortcuts - kan tilgås ved File/Edit > Keymap):
```cson
'atom-workspace atom-text-editor:not([mini])':
    'ctrl-shift-x': 'editor:toggle-line-comments'
```

#### Stylesheet
Dette er mine nuværrende ændringer til temaet (atom material + Base 16 Tomorrow Dark)
```less
atom-text-editor {
  text-rendering: optimizeLegibility;
}

/*
Turn off ligatures inside of strings and regular expressions
 */
atom-text-editor.editor .syntax--string.syntax--quoted,
atom-text-editor.editor .syntax--string.syntax--regexp {
  -webkit-font-feature-settings: "liga" off, "calt" off;
}

atom-workspace {
    font-size: 1em;
    line-height: 1.3;
}

.tree-view .list-nested-item {
    padding: 0.15em 0;
}

.pane-item section .section-heading,
.pane-item .section .section-heading,
.pane-item section .section-heading.icon::before,
.pane-item .section .section-heading.icon::before{
    font-size: 1.7em;
    font-weight: 300;
}

.settings-view .breadcrumb + .section {
    padding-bottom: 0;
}

.settings-view .sub-section .sub-section-heading {
    font-size: 1.3em;
}

.settings-view .setting-title,
.form-control {
    font-size: 1em;
}

.settings-view .package-card {
    font-size: 1.1em;
}

.overlay, atom-panel.modal{
    font-size: 1.1em;
}

atom-text-editor[mini] {
    font-size: 1em;
}

/*
Git colors
 */

//Modified
.list-group li:not(.list-nested-item).status-modified,
.list-tree li:not(.list-nested-item).status-modified,
.list-group li.list-nested-item.status-modified > .list-item,
.list-tree li.list-nested-item.status-modified > .list-item
{
    color: hsl(30, 50%, 50%);
}

.list-group li:not(.list-nested-item).selected.status-added,
.list-tree li:not(.list-nested-item).selected.status-added,
.list-group li.list-nested-item.selected.status-added > .list-item,
.list-tree li.list-nested-item.selected.status-added > .list-item
{
    color: hsl(80, 50%, 50%);
}


/**
 * Indent guide color
 */
atom-text-editor .indent-guide {
    color: rgba(80,80,80,0.25);
}
```
