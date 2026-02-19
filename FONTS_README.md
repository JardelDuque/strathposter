# University of Strathclyde Brand Fonts Setup

## Required Fonts

Your poster now uses the official University of Strathclyde brand fonts:

### Meta OT
- **Meta OT Normal** - Default body text
- **Meta OT Bold** - Headings in body copy
- **Meta OT Normal Italic** - Italic text
- **Meta OT Bold Italic** - Bold italic text

### ClanOT
- **ClanOT Black** - Headlines and headline quotes
- **ClanOT Bold** - Subheadings, callout text, quotes
- **ClanOT Medium** - Subheadings, callout text, intro copy

## Installation Steps

### Option 1: Place Fonts in Local Directory (Recommended)
1. Obtain the font files from your University IT or Marketing department
2. Copy the `.otf` font files to the `fonts/` folder in your poster directory:
   ```
   fonts/
   ├── MetaOT-Normal.otf
   ├── MetaOT-Bold.otf
   ├── MetaOT-NormalItalic.otf
   ├── MetaOT-BoldItalic.otf
   ├── ClanOT-Black.otf
   ├── ClanOT-Bold.otf
   └── ClanOT-Medium.otf
   ```

### Option 2: Install Fonts System-Wide
1. Install the fonts on your system (Windows: Right-click → Install)
2. Update `poster.tex` to remove the `Path = fonts/,` line from font definitions

## Compiling the Poster

**Important:** You must now use **XeLaTeX** or **LuaLaTeX** instead of pdflatex.

### Using latexmk (Recommended)
```powershell
latexmk -xelatex poster.tex
```

### Using XeLaTeX directly
```powershell
xelatex poster.tex
```

### In your IDE
- **VS Code with LaTeX Workshop**: Add to `.vscode/settings.json`:
  ```json
  {
    "latex-workshop.latex.recipes": [
      {
        "name": "xelatex",
        "tools": ["xelatex"]
      }
    ]
  }
  ```
- **TeXstudio**: Options → Configure → Build → Default Compiler → Select "XeLaTeX"
- **Overleaf**: Menu → Compiler → Select "XeLaTeX"

## Font Usage in LaTeX

### Commands Available

```latex
% Body text (automatic with Meta OT)
This is regular body text.
\textbf{This is bold text} for emphasis.

% Headlines (ClanOT Black)
\headline{Main Headline Here}

% Subheadings (ClanOT Bold)
\subheading{Subheading Text}

% Callouts and quotes (ClanOT Medium)
\callout{Important callout or quote}

% Direct font access
{\clanblack Large headline text}
{\clanbold Subheading text}
{\clanmedium Medium weight text}
```

### Typography Examples in Your Poster

The poster file now includes complete examples showing:
- Body text hierarchy with Meta OT Normal and Bold
- Headlines using ClanOT Black
- Subheadings with ClanOT Bold
- Callouts and quotes with ClanOT Medium
- Integration with mathematical notation

## Troubleshooting

### Font not found error
If you get a font error:
1. Verify font files are in the `fonts/` directory
2. Check font file names match exactly (case-sensitive)
3. Ensure you're compiling with XeLaTeX, not pdflatex

### Missing fonts?
Contact your University Marketing or IT department:
- **University of Strathclyde Marketing**: marketing@strath.ac.uk
- Request access to brand font files for academic posters

### Alternative: Test Without Fonts
To test the layout before obtaining fonts, temporarily replace with system fonts:
```latex
\setmainfont{Arial}
\newfontfamily\clanblack{Arial Black}
\newfontfamily\clanbold{Arial}[BoldFont = *-Bold]
\newfontfamily\clanmedium{Arial}
```

## Brand Guidelines Reference

- **Meta OT**: Body text only, NOT for promotional headings
- **ClanOT**: Headlines, subheadings, display text
- **Arial**: Only for internal documents (NOT for posters)

Refer to the University's [Brand Guidelines](https://www.strath.ac.uk/staff/brandguidelines/) for full details.
