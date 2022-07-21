# sphinx-hoverxref - preview cross-references

Using sphinx-hoverxref, we can preview cross-references in the documentation.

For instance, try placing your mouse over {hoverxref}`this reference to the front page <intro>`.
We have used a named "target" for the reference. Here are some examples of how to name your targets:

```{tab} reStructuredText

```rest
.. _foobar:

My Headline
===========

Here is a paragraph, we link to this headline :hoverxref:`like this <foobar>`
```

```{tab} MyST

```markdown

 (foobar)=
 
 # My Headline
 
 Here is a paragraph, we link to this headline {hoverxref}`like this <foobar>`.
```
