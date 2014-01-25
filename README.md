SJTU XeTeX-LaTeX Thesis Template
======

What's this? 
-------

This is (Xe)LaTeX template for thesis of Shanghai Jiaotong University. Currently, templates for bachelor, master, and Ph.D thesis are released in three different branches separately. You can download the zip packages from the following links. 

* [SJTU Bachelor Thesis Template Download](https://github.com/weijianwen/sjtu-thesis-template-latex/archive/bachelor-thesis.zip)
* [SJTU Master Thesis Template Download](https://github.com/weijianwen/sjtu-thesis-template-latex/archive/master-thesis.zip) 
* [SJTU Ph.D Thesis Template Download](https://github.com/weijianwen/sjtu-thesis-template-latex/archive/phd-thesis.zip) 

The original version of this template dated back about two years ago, when CJK-latex was still the most prevalent solution for TeX/LaTeX to handle CJK (Chinese, Japanese, Korean) characters. A nice guy at the school of physics, SJTU, made a LaTeX template for Ph.D thesis and posted on SJTU's [BBS](https://bbs.sjtu.edu.cn/bbsdoc?board=TeX_LaTeX). I followed his steps, added some refinement and documentations, and made the template more accessible for general people.

In the *CJK-latex* age, one of the intimidating things for LaTeX newbie was setting up a usable Chinese LaTeX environment. It took me quite a long time to figure out how those things, such *latex, dvipdfmx, pdflatex, bibtex, dvips, et al.* worked together and shared my experiences on BBS board. However, most of my time had been spent on struggling with the CJK issues and solving wired problems, which, at most time, were caused by not following the steps exactly. That mess-up situation made me kind of frustrated, because little improvement towards the template required much much more verification and adjustment. I called it *CJK package hell*.

Therefore, I took no hesitation to switch the template to XeTeX/XeLaTeX when XeTeX seemed mature enough. It had been a really wise decision. With the help of other warm-hearted guys, SJTU thesis templates were ported to XeTeX and released during the days when lots of master candidates were fighting with their thesis. Though the SJTU XeTeX-based template had never become a hot topic of any kind, being helpful to others, I think, had been the most valuable reward for me. I really appreciated all the guys who used the template and send back their feedback.

I used this template to finish my master thesis, and decided to make the template *code-freeze*. Being XeTeX-based is the current state of the template and still works well. I made a last commit to the template one year ago, giving a stop at that time.

But, I think the template is still in a *primitive* state, far from a *generally-nice* work. As my understanding about TeX, Git, document preparing grows, I think it's time to refresh the template. GitHub is a place full of all kinds of geniuses, thus I host my project here in hope for receiving all kinds of refinement or feedback. 

TODO
------
* Merge the bachelor, master and Ph.D thesis into one.
* The layout units look ugly.
* 用中文重写这份README.
* 使用良好的"LaTeX代码风格"改写文档源代码
	* 使用 \command{body} 形式调用命令；
	* 避免在模板中使用 plain TeX 代码；
* Add a ```sjtuthesiscmd.cfg```?
* Move natbib's configuration to other part. \RequirePackage[sort&compress,numbers]{natbib}
* Figure out which parts can be configured in ```sjtuthesis.cfg```

How to use it?
------

### Prerequisites

* A usable XeTeX/XeLaTeX instance. The latest [CTeX], [TeXLive] and [MacTeX] are OK.
* [TeX Gyre Font] collection which are used as main ASCII fonts.
* Some available Chinese fonts. 

### Compile the sample document

Type the following commands and a file named ```diss.pdf``` will be generated.

	$ cd $YOUR_WORK_DIR
	$ xelatex -no-pdf --interaction=nonstopmode diss
	$ bibtex diss
	$ xelatex -no-pdf --interaction=nonstopmode diss
	$ xelatex --interaction=nonstopmode diss
 
Or, you can use the GNUMake tool.

	$ make && make view

A [HOWTO.pdf] is shipped with the project, which explains the usage further.

# How to contribute? 

Contributions toward this project include, but *not limited* to the following work. 

* Use the template and report an [issue] when encountering problems.
* Fork and refine the documents (README, Wiki, et al.).
* Fork and refine the template according to the tasks listed in *TODO*.
* Tell other guys the ```SJTU-XeLaTeX-Template``` is hosted here on github. 

# FAQs and not-so-FAQs 

Q: Is this template "official"?

A: No. SJTU has not yet released its official TeX template for composing thesis. We make this template according to the officially-stated layout requirements and add some refinements because of aesthetic consideration.

Q: Is thesis in ```PDF``` formats suitable for submitting?

A: Absolutely yes. ```PDF``` is portable file format, and your PDF documents will look exactly the same as the hard-copy ones no matter what applications are used for viewing. It is totally unreasonable not accepting a PDF-formated thesis. The fact, as far as I know, is that, the SJTU library happily accepts all PDF thesis.

Q: @farseerfc hosts a project named [sjtu-thesis-xelatex] on github. Is this the same thing?

A: Hmm... Let me explain.  @farseerfc's code was based on my template and adapted to bachelor-thesis format. I really appreciate his contributions and hope to merge his changes into my repo if possible (not now but in the future). However, due to strong personality, I keep in mind that the git repo for SJTU-XeTeX-template should be in 100% control of mine and progresses exactly in the pace I set. Therefore, I create this repo along with the tasks listed in TODO. These tasks should differentiate my repo from other similar projects.

# See more
[README.pdf]: https://raw.github.com/weijianwen/sjtu-thesis-template-latex/master/README.pdf
[CTeX]: http://www.ctex.org/
[TeXLive]: http://www.tug.org/texlive/
[MacTeX]: http://tug.org/mactex/
[TeX Gyre Font]: http://www.gust.org.pl/projects/e-foundry/tex-gyre/
[LATEX Notes]: http://math.nju.edu.cn/~meijq/tex/lnotes.pdf
[XeTeX/中文排版之胡言乱语]: http://goo.gl/oRNcW

# Update History 
* Last update: May 26, 2013
* Dec 27, 2012. v0.5.2 is released. Fix typos.
* Dec 5, 2012. v0.5 is released. Add Makefile; refine the manual (README.pdf); replace xltxtra pacakge with metalog; replace amsmath package with mathtools.
* May 30, 2012. v0.4 is released. Reopen this project. Add README.
* Jan 23, 2011. Finish my master thesis. Code freeze.
