---
title:  Vim LaTeX Workflow
layout: post
tags:
  - tutorial
  - workflow
  - LaTeX
---

LaTeX is a document preparation system that encourages authors to
focus on getting the right content, rather than being bogged down in
formatting and appearance. It's not a perfect analogy, but think of
how HTML and CSS separate the concerns of content and style. Using
LaTeX to write a document is like writing a webpage without having to
use CSS at all (though the option for more fine-grained control is
certainly there).

<!-- MORE -->

I've challenged myself to learn LaTeX and use it to replace Word
wherever I can. After all, according to the [project<i class="fa
fa-external-link"></i>][latex home]{:target="_blank"}:

> LaTeX is the de facto standard for the communication and
> publication of scientific documents.

[latex home]: https://www.latex-project.org

To this end, I've rewritten my company-internal resume (and am
working on my personal resume) using LaTeX, and I wanted to share my
workflow with you because I found it to be pretty smooth. It's based
loosely on [Luke Smith's<i class="fa fa-external-link"></i>][luke
smith]{:target="_blank"} LaTeX tutorials. In short, you write your
LaTeX source code in vim, and whenever you save the file, your
preview window updates to show you what the compiled document looks
like, no need to lift a finger.

[luke smith]: http://lukesmith.xyz/latex.html

## Materials

Naturally you'll first need to obtain LaTeX for your system. You can
find downloads for any platform [here<i class="fa
fa-external-link"></i>][downloads]{:target="_blank"}. My work laptop
that I set this up on is a Mac, so I'm using the full version of
[MacTex<i class="fa fa-external-link"></i>][mactex]{:target="_blank"}
(I'd be interested to hear if this workflow works without any
glitches on the [smaller distribution<i class="fa
fa-external-link"></i>][small]{:target="_blank"}).

[downloads]: https://www.latex-project.org/get
[mactex]: http://www.tug.org/mactex/mactex-download.html
[small]: http://www.tug.org/mactex/morepackages.html

Next, you'll need the [vimtex<i class="fa
fa-external-link"></i>][vimtex]{:target="_blank"} plugin for vim. In
addition to the live-compile and -preview functions, this will also
provide vim with smarter syntax highlighting, and extra text objects
and movements for navigating (if you aren't sure what these latter
two features mean, check out the `vimtutor` command at your command
line). Please note that the keybindings for vimtex all start with the
`localleader` (`\` by default) so if you've remapped this, the
shortcuts will be a little different.

[vimtex]: https://github.com/lervag/vimtex

![vimtex commands][vimtex gif]

[vimtex gif]: https://github.com/lervag/vimtex/raw/master/media/quick_start.gif?raw=true

<p style="text-align:center">
<small><i>vimtex commands (<a href="https://github.com/lervag/vimtex" target="_blank">source<i class="fa fa-external-link"></i></a>)</i></small>
</p>

There are several other options for vim plugins that will give you
the live preview functionality (Luke Smith, for instance, recommends
[vim-live-latex-preview<i class="fa fa-external-link"></i>][vim
live]{:target="_blank"}) but I chose vimtex because of it's the most
minimal and, for lack of a better word, vim-like.  It knows what it
is and doesn't try to be more, and the provided movements and text
objects integrate really seamlessly with the way I interact with text
through vim.

[vim live]: https://github.com/ying17zi/vim-live-latex-preview

Finally, you'll need a PDF viewer supported by vimtex. You can find a
full list of supported programs in vimtex's README. I did a little
experimenting and found that [Skim<i class="fa
fa-external-link"></i>][skim]{:target="_blank"} worked the best on my
machine.

[skim]: https://skim-app.sourceforge.io

## Procedure

Once everything is installed, specify which PDF viewer you're using
by putting a line like this in your vimrc:

    let g:vimtex_view_method = 'skim'

Run `:help vimtex_view_method` in vim for details like the list of
options.

Now close vim, and open up a LaTeX document. In normal mode, hit
`\ll` to start auto-compiling, and `\lv` to pop open your preview
window. That's it! In my particular workflow in this Mac, I use a
full split screen with my terminal (with the source code open in vim)
on the left and the Skim preview window on the right.

## Conclusion

Hopefully having a really smooth workflow for creating documents will
help encourage you to use LaTeX a little more. I know that was a
blocker for me at first, the fact that I had to use [Overleaf<i
class="fa fa-external-link"></i>][overleaf]{:target="_blank"}, an
online tool, to get a live preview window.  Now LaTeX is a little
closer at hand, and I look forward to using it more and more in the
future.

[overleaf]: https://www.overleaf.com
