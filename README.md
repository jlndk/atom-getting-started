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
* Jeg er ikke en scrub, men hvis i har nogle gode light themes kan i bare PM'e mig

### CUSTOMIZATIONS:
keymap (custom shortcuts - kan tilgås ved File/Edit > Keymap):
```cson
'atom-workspace atom-text-editor:not([mini])':
    'ctrl-shift-x': 'editor:toggle-line-comments'
```
