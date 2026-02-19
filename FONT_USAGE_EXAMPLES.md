# Quick Font Usage Reference

## Standard Text Formatting

```latex
% Regular body text - Meta OT Normal (automatic)
This is regular paragraph text that will use Meta OT Normal by default.

% Bold emphasis - Meta OT Bold
\textbf{This text is bold} and uses Meta OT Bold.

% Italic text - Meta OT Normal Italic  
\textit{This text is italic} and uses Meta OT Normal Italic.

% Bold italic - Meta OT Bold Italic
\textbf{\textit{This is bold italic}} using Meta OT Bold Italic.
```

## Headlines (ClanOT Black)

```latex
% Use for major section headlines
\headline{Major Research Finding}

% Or use directly with size control
{\clanblack\Huge Main Title}
{\clanblack\LARGE Section Headline}
```

## Subheadings (ClanOT Bold)

```latex
% Use for subsection headings
\subheading{Research Methodology}

% Or with manual sizing
{\clanbold\Large Subsection Title}
```

## Callouts & Quotes (ClanOT Medium)

```latex
% For highlighted text, quotes, or callout boxes
\callout{This is an important takeaway message}

% For block quotes
\callout{"Typography is the visual voice of written words"}

% Manual usage
{\clanmedium\large Key finding or statistic}
```

## Combined Examples

```latex
\begin{posterbox}[name=example]{Box Title}

\headline{Understanding Climate Change}

\subheading{Current Challenges}

The research demonstrates significant findings in environmental science. 
Recent studies show \textbf{critical evidence} supporting our hypothesis.

\callout{Key Finding: Temperature rise of 1.5°C by 2030}

Further analysis reveals additional patterns. The \textit{correlation} 
between variables suggests \textbf{strong causal relationships}.

\end{posterbox}
```

## Typography Hierarchy

From largest to smallest visual impact:

1. **ClanOT Black** - Main headlines, poster title
2. **ClanOT Bold** - Section subheadings  
3. **ClanOT Medium** - Callouts, quotes, emphasis
4. **Meta OT Bold** - Bold text within body copy
5. **Meta OT Normal** - Standard body text

## Do's and Don'ts

### ✓ DO:
- Use ClanOT for display typography (headlines, subheadings)
- Use Meta OT for all body text and paragraphs
- Use consistent hierarchy throughout your poster
- Mix font weights to create visual interest

### ✗ DON'T:
- Don't use Arial on promotional materials (posters are promotional!)
- Don't use too many font weights in one block
- Don't use ClanOT for long paragraphs (readability issues)
- Don't manually specify fonts when commands exist

## Size Guidelines for A0 Poster

```latex
% With fontscale=0.25, these work well:
\headline{...}      % ClanOT Black - automatically sized
\subheading{...}    % ClanOT Bold - automatically sized
\callout{...}       % ClanOT Medium - automatically sized

% Manual sizing if needed:
\Huge          % Largest
\huge          % Very large
\LARGE         % Large
\Large         % Medium-large
\large         % Medium
\normalsize    % Body text (default)
```

## Working with Math

Fonts work seamlessly with LaTeX math:

```latex
Body text explaining the equation:

\[
E = mc^2
\]

\textbf{Where:} $E$ is energy, $m$ is mass, and $c$ is speed of light.
```

## Contact for University Fonts

If you don't have the font files:
- Email: marketing@strath.ac.uk
- Subject: "Request for Brand Font Files - Academic Poster"
- Mention you need Meta OT and ClanOT for PhD conference poster
