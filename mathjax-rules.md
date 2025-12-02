Pages to fix:
- Basis
- Cauchy Schwarz Inequality
- Composition
- Determinant
- Echelon form
- Eigenvalues and eigenvectors
- Identity matrix
- Inverse image
- Matrix multiplication
- Series

MathJax TeX and LaTeX Support
The support for TeX and LaTeX in MathJax consists of two parts: the tex2jax preprocessor, and the TeX input processor. The first of these looks for mathematics within your web page (indicated by math delimiters like $$...$$) and marks the mathematics for later processing by MathJax. The TeX input processor is what converts the TeX notation into MathJax’s internal format, where one of MathJax’s output processors then displays it in the web page.

The tex2jax preprocessor can be configured to look for whatever markers you want to use for your math delimiters. See the tex2jax configuration options section for details on how to customize the action of tex2jax.

The TeX input processor handles conversion of your mathematical notation into MathJax’s internal format (which is essentially MathML), and so acts as a TeX to MathML converter. The TeX input processor has few configuration options (see the TeX options section for details), but it can also be customized through the use of extensions that define additional functionality (see the TeX and LaTeX extensions below).

Differences
Since MathJax renders for the web and TeX is a print layout engine, there are natural limitations of which parts of TeX can be supported in a reasonable way. Accordingly, there are several differences between “real” TeX/LaTeX systems and MathJax’s TeX Input.

First and foremost, the TeX input processor implements only the math-mode macros of TeX and LaTeX, not the text-mode macros. MathJax expects that you will use standard HTML tags to handle formatting the text of your page; it only handles the mathematics. So, for example, MathJax does not implement \emph or \begin{enumerate}...\end{enumerate} or other text-mode macros or environments. You must use HTML to handle such formatting tasks. If you need a LaTeX-to-HTML converter, you should consider other options.

There are two exception to this rule. First, MathJax supports the \ref macro outside of math-mode. Second, MathJax supports some macros that add text within math-mode (such as \text{}) as well as $...$ within such macros (to switch back into math-mode) and \$ to escape.

Second, some features in MathJax might be necessarily limited. For example, MathJax only implements a limited subset of the array environment’s preamble, i.e., only the l, r, c, and | characters alongside : for dashed lines; everything else is ignored.

Note

If you are not familiar with TeX/LaTeX, a good starting point is the LaTeX Wiki book.

TeX and LaTeX math delimiters
By default, the tex2jax preprocessor defines the LaTeX math delimiters, which are \(...\) for in-line math, and \[...\] for displayed equations. It also defines the TeX delimiters $$...$$ for displayed equations, but it does not define $...$ as in-line math delimiters. That is because dollar signs appear too often in non-mathematical settings, which could cause some text to be treated as mathematics unexpectedly. For example, with single-dollar delimiters, “… the cost is $2.50 for the first one, and $2.00 for each additional one …” would cause the phrase “2.50 for the first one, and” to be treated as mathematics since it falls between dollar signs. For this reason, if you want to use single-dollars for in-line math mode, you must enable that explicitly in your configuration:

MathJax.Hub.Config({
  tex2jax: {
    inlineMath: [['$','$'], ['\\(','\\)']],
    processEscapes: true
  }
});
Note that if you do this, you may want to also set processEscapes to true, as in the example above, so that you can use \$ to prevent a dollar sign from being treated as a math delimiter within the text of your web page. (Note that within TeX mathematics, \$ always has this meaning; processEscapes only affects the treatment of the opening math delimiter.)

Note that, as opposed to true LaTeX, MathJax processes all environments when wrapped inside math delimiters. By defaut, MathJax will also render all environments outside of delimiters; this can be controlled via the processEnvironments option in the tex2jax configuration options.

See the config/default.js file, or the tex2jax configuration options page, for additional configuration parameters that you can specify for the tex2jax preprocessor, which is the component of MathJax that identifies TeX notation within the page.

TeX and LaTeX in HTML documents
Keep in mind that your mathematics is part of an HTML document, so you need to be aware of the special characters used by HTML as part of its markup. There cannot be HTML tags within the math delimiters (other than <br>) as TeX-formatted math does not include HTML tags. Also, since the mathematics is initially given as text on the page, you need to be careful that your mathematics doesn’t look like HTML tags to the browser (which parses the page before MathJax gets to see it). In particular, that means that you have to be careful about things like less-than and greater-than signs (< and >), and ampersands (&), which have special meaning to the browsers. For example,

... when $x<y$ we have ...
will cause a problem, because the browser will think <y is the beginning of a tag named y (even though there is no such tag in HTML). When this happens, the browser will think the tag continues up to the next > in the document (typically the end of the next actual tag in the HTML file), and you may notice that you are missing part of the text of the document. In the example above, the “we have ...” will not be displayed because the browser thinks it is part of the tag starting at <y. This is one indication you can use to spot this problem; it is a common error and should be avoided.

Usually, it is sufficient to simply put spaces around these symbols to cause the browser to avoid them, so

... when $x < y$ we have ...
should work. Alternatively, you can use the HTML entities &lt;, &gt; and &amp; to encode these characters so that the browser will not interpret them, but MathJax will. E.g.,

... when $x &lt; y$ we have ...
Finally, there are \lt and \gt macros defined to make it easier to enter < and > using TeX-like syntax:

... when $x \lt y$ we have ...
Keep in mind that the browser interprets your text before MathJax does.

Another source of difficulty is when MathJax is used in content management systems that have their own document processing commands that are interpreted before the HTML page is created. For example, many blogs and wikis use formats like Markdown to allow you to create the content of your pages. In Markdown, the underscore is used to indicate italics, and this usage will conflict with MathJax’s use of the underscore to indicate a subscript. Since Markdown is applied to the page first, it will convert your subscript markers into italics (inserting <i> or <em> tags into your mathematics, which will cause MathJax to ignore the math).

Such systems need to be told not to modify the mathematics that appears between math delimiters. That usually involves modifying the content-management system itself, which is beyond the means of most page authors. If you are lucky, someone else will already have done this for you, and you can find a MathJax plugin for your system on the MathJax-In-Use page.

If there is no plugin for your system, or if it doesn’t handle the subtleties of isolating the mathematics from the other markup that it supports, then you may have to “trick” it into leaving your mathematics untouched. Most content-management systems provide some means of indicating text that should not be modified (“verbatim” text), often for giving code snippets for computer languages. You may be use that to enclose your mathematics so that the system leaves it unchanged and MathJax can process it. For example, in Markdown, the back-tick (`) is used to mark verbatim text, so

... we have `\(x_1 = 132\)` and `\(x_2 = 370\)` and so ...
may be able to protect the underscores from being processed by Markdown.

Some content-management systems use the backslash (\) as a special character for “escaping” other characters, but TeX uses this character to indicate a macro name. In such systems, you may have to double the backslashes in order to obtain a single backslash in your HTML page. For example, you may have to do

\\begin{array}{cc}
  a & b \\\\
  c & c
\\end{array}
to get an array with the four entries a, b, c, and d. Note in particular that if you want \\ you will have to double both backslashes, giving \\\\.

Finally, if you have enabled single dollar-signs as math delimiters, and you want to include a literal dollar sign in your web page (one that doesn’t represent a math delimiter), you will need to prevent MathJax from using it as a math delimiter. If you also enable the processEscapes configuration parameter, then you can use \$ in the text of your page to get a dollar sign (without the backslash) in the end. Alternatively, you use something like <span>$</span> to isolate the dollar sign so that MathJax will not use it as a delimiter.

