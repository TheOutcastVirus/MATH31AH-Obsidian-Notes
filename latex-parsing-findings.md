# LaTeX/MathJax Parsing Error Analysis

## Date
2025-12-02

## Overview
This document contains findings from investigating LaTeX formatting errors in markdown files listed in `mathjax-rules.md`. The analysis includes common MathJax parsing issues and specific errors found in the problematic files.

## Common MathJax Parsing Issues

### 1. Math Delimiters (Obsidian/Markdown Configuration)
- **RECOMMENDED for Obsidian**:
  - `$...$` for inline math
  - `$$...$$` (on separate lines) for display/block math
- **AVOID**: `\[...\]` and `\(...\)`
  - **Reason**: Backslashes conflict with Markdown escape sequences
  - Markdown processes the document before MathJax, causing delimiter conflicts
  - The backslash is a special character in both Markdown (for escaping) and TeX (for macros)
- **Critical**: All delimiters must be properly matched and closed
- **Whitespace rule**: In Obsidian, inline math `$...$` requires no whitespace before the closing `$`

### 2. Markdown vs LaTeX Conflicts
**Critical Issue**: Markdown processes documents BEFORE MathJax, causing character conflicts:

- **Underscore conflict**:
  - Markdown uses `_` for italics
  - LaTeX uses `_` for subscripts
  - Markdown will insert `<i>` or `<em>` tags, breaking MathJax
  - **Solution**: Keep math inside proper `$...$` delimiters to protect from Markdown processing

- **Backslash conflict**:
  - Markdown uses `\` to escape special characters
  - TeX uses `\` to indicate macro names
  - This is why `\[` and `\]` delimiters are problematic in Markdown
  - **Solution**: Use `$` and `$$` delimiters instead

- **Asterisk conflict**:
  - Markdown uses `*` for italics/bold
  - Can interfere with math notation using asterisks
  - **Solution**: Keep asterisks inside math delimiters

### 3. Special HTML Characters
Mathematics in MathJax is part of an HTML document, so special characters can cause conflicts:
- **Less-than/greater-than signs**: `<`, `>` have special meaning to browsers
- **Ampersands**: `&` is a special HTML character
- **Issue**: Browsers parse the page before MathJax processes it, so math that looks like HTML tags can be misinterpreted

### 4. Delimiter Matching Errors
- Missing or unrecognized delimiters for `\left` and `\right` commands
- All opening delimiters must have corresponding closing delimiters
- Parentheses, brackets, and braces in math mode must be properly balanced

### 5. Enabling Single Dollar Signs (When Needed)
For systems where `$...$` is not enabled by default, you can configure MathJax:

**MathJax 4.0**:
```javascript
window.MathJax = {
  tex: {
    inlineMath: {'[+]': [['$', '$']]}
  }
};
```

**MathJax 3.x**:
```javascript
window.MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']]
  }
};
```

**Note**: Obsidian already supports `$...$` by default, so this configuration is not needed.

## Specific Errors Found in Files

### 1. Cauchy Schwarz Inequality.md
**Location**: Line 34
**Error**: Missing closing pipe character
**Current**: `||v||\cdot|w||`
**Should be**: `||v||\cdot||w||`
**Issue**: The norm notation for `w` is missing a closing pipe, which breaks the LaTeX parsing.

### 2. Echelon form.md
**Location**: Line 19
**Error**: Asterisk usage in math mode
**Current**: `1* & 1 & 0 & 0 & 0`
**Potential issue**: The asterisk `*` after `1` could be interpreted as markdown italics delimiter rather than mathematical notation. While this is inside a math block (which should protect it), it's worth verifying.
**Recommendation**: If asterisks are meant to denote pivots, consider using `1^* ` (superscript) or `\boxed{1}` for clearer notation.

### 3. Identity matrix.md
**Location**: Line 27
**Error**: Mathematical notation outside math delimiters
**Current**: `- You can also write this as $(a_{ij})_{n,n}, a_{ij} = 1, i = j, =0, i \neq j$`
**Issue**: The conditional definition `a_{ij} = 1, i = j, =0, i \neq j` appears to have improper structure.
**Should be**: Consider rewriting as:
```
- You can also write this as $(a_{ij})_{n,n}$ where $a_{ij} = 1$ if $i = j$ and $a_{ij} = 0$ if $i \neq j$
```
Or use proper cases notation:
```
$$
a_{ij} = \begin{cases}
1 & \text{if } i = j \\
0 & \text{if } i \neq j
\end{cases}
$$
```

### 4. Basis.md
**Location**: Lines throughout
**Status**: No obvious LaTeX errors detected
**Note**: All math delimiters appear properly matched

### 5. Composition.md
**Location**: Lines throughout
**Status**: No obvious LaTeX errors detected
**Note**: All math delimiters appear properly matched

### 6. Determinant.md
**Location**: Lines throughout
**Status**: No obvious LaTeX errors detected
**Note**: Matrix notation and determinant formulas appear correctly formatted

### 7. Eigenvalues and eigenvectors.md
**Location**: Lines throughout
**Status**: No obvious LaTeX errors detected
**Note**: Complex mathematical notation appears properly formatted

### 8. Inverse image.md
**Location**: Lines throughout
**Status**: No obvious LaTeX errors detected
**Note**: All math delimiters appear properly matched

### 9. Matrix multiplication.md
**Location**: Lines throughout
**Status**: No obvious LaTeX errors detected
**Note**: References to embedded images (`![[...]]`) are present but should not affect LaTeX parsing

### 10. Series.md
**Location**: Lines throughout
**Status**: No obvious LaTeX errors detected
**Note**: Sum notation appears correctly formatted

## Recommendations

### Immediate Fixes Required
1. **Cauchy Schwarz Inequality.md:34** - Add missing pipe character
2. **Identity matrix.md:27** - Restructure conditional notation

### Best Practices Going Forward
1. **Use `$...$` for inline math** - Simple and Markdown-friendly
2. **Use `$$...$$` on separate lines for display math** - Avoid `\[...\]` due to backslash conflicts
3. **No whitespace before closing `$`** - Obsidian requires tight spacing for inline math
4. **Ensure all norm notations `||...||` have matching pipes** - Critical for proper rendering
5. **Use proper cases notation for piecewise definitions** - Clearer than inline conditionals
6. **Verify all `\left` commands have matching `\right` commands** - Prevents delimiter errors
7. **Keep math delimiters properly balanced** - Mismatched delimiters break rendering
8. **Protect special characters inside math delimiters** - Prevents Markdown from processing them
9. **Use `\$` for literal dollar signs** - When you need to display currency
10. **Avoid using `<`, `>`, `&` directly in math** - Use `\lt`, `\gt`, `\&` if needed

## Testing Recommendations
1. Test each fixed file in your Obsidian/MathJax renderer
2. Verify that all mathematical expressions render correctly
3. Check for any residual parsing errors in the browser console
4. Ensure markdown formatting doesn't interfere with math mode

## Sources
- [MathJax TeX and LaTeX Support — MathJax 2.7 documentation](https://docs.mathjax.org/en/v2.7/tex.html)
- [TeX and LaTeX math delimiters — MathJax 4.0 documentation](https://docs.mathjax.org/en/latest/input/tex/delimiters.html)
- [TeX and LaTeX math delimiters — MathJax 3.0 documentation](https://docs.mathjax.org/en/v3.0-latest/input/tex/delimiters.html)
- [Configuring MathJax — MathJax 4.0 documentation](https://docs.mathjax.org/en/latest/web/configuration.html)
- [MathJax Parenthesis - Missing or unrecognized delimiter - Stack Overflow](https://stackoverflow.com/questions/61536748/mathjax-parenthesis-missing-or-unrecognized-delimiter-for-right)
- [How to Write Mathematical Notations in Obsidian - MakeUseOf](https://www.makeuseof.com/write-mathematical-notation-obsidian/)
- [MathJax in Obsidian - Andrex Ibiza](https://andrexibiza.substack.com/p/mathjax-in-obsidian)
- [Inline Math Rendering with two dollar signs - Obsidian Forum](https://forum.obsidian.md/t/inline-math-rendering-with-two-dollar-signs/79966)
