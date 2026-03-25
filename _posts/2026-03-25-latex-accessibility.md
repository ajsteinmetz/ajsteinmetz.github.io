---

layout: post
title: "Accessibility for LaTeX-Based Teaching"
categories: mathematics
tags: latex accesibility education
---


## Accessibility for LaTeX-Based Teaching

On April 26, 2026, we are required as educators to comply with the [new ADA Title II standards](https://digitalaccess.gatech.edu/title-ii/requirements) which adhere to [Web Content Accessibility Guidelines (WCAG) 2.1 Level AA](https://www.w3.org/TR/WCAG21/). I regularly prepare mathematical and physics-heavy teaching materials using GitHub, Overleaf, and LaTeX. Because these documents often contain substantial mathematical notation, accessibility requires some extra care.

From reviewing the current landscape, I think of the available options as falling into **two broad branches**:

1. **Make LaTeX-generated PDFs more accessible**, primarily through PDF tagging and related metadata.
2. **Move away from PDF-first workflows** and instead render LaTeX source into more output-agnostic formats such as HTML, EPUB, web pages, or other digital-first formats.

This page collects resources I have found useful while exploring both paths and then I complain at the end -- which is only fitting.

---

## 1. Accessible PDF workflows in LaTeX

This approach keeps LaTeX as the authoring environment and aims to produce **tagged PDFs** that work better with screen readers and other assistive technologies.

My present impression is that this is a promising and rapidly improving area, but still one under active development.

### Good starting points

- <a href="https://hunterlehmann.github.io/accessibility/latex101/">Accessible LaTeX 101</a> -- Dr. Hunter Lehmann's concise getting-started guide for accessible LaTeX documents.
- <a href="https://hunterlehmann.github.io/accessibility/latex/">Accessible LaTeX</a> -- Dr. Lehmann's broader resource page, including a reference guide, workshop links, example documents, and additional resources.
- <a href="https://www.overleaf.com/learn/latex/An_introduction_to_tagged_PDF_files%3A_internals_and_the_challenges_of_accessibility">An introduction to tagged PDF files: internals and the challenges of accessibility</a> -- Overleaf article on the technical background of tagged PDFs.
- <a href="https://docs.overleaf.com/writing-and-editing/creating-accessible-pdfs">Creating accessible PDFs in LaTeX</a> -- Overleaf documentation focused on practical guidance.
- <a href="https://latex3.github.io/tagging-project/documentation/usage-instructions">LaTeX Tagging Project: usage instructions</a> -- central project documentation for LaTeX tagging support.

### Institution and support resources

- <a href="https://blog.ctl.gatech.edu/2025/09/12/title-ii-web-accessibility-canvas-what-the-new-guidelines-mean-for-you/"> Georgia Tech Center for Teaching and Learning: Title II Web Accessibility & Canvas: What the New Guidelines Mean for You</a>
- <a href="https://ets.osu.edu/digital-accessibility/latex-accessibility-guide">Ohio State Engineering Technology Services: LaTeX Accessibility Guide</a>
- <a href="https://esail.tamu.edu/faculty-tutorials/accessible-latex-pdf-ua-2-overleaf-2025/">Texas A&amp;M eSAIL: Creating Accessible LaTeX PDFs: PDF/UA-2 Compliance in Overleaf</a>
- <a href="https://academictech.uchicago.edu/2025/01/17/create-accessible-equations-and-formulas-with-latex-canvas-and-overleaf/">University of Chicago: Create Accessible Equations and Formulas with LaTeX, Canvas, and Overleaf</a>

### Notes on slides and presentations

Traditional `beamer` for LaTeX generated slides is not and will never be supported for PDF Tagging and accessibility. A newer alternative is:

- <a href="https://ctan.org/pkg/ltx-talk">`ltx-talk`</a> -- a newer LaTeX class aimed at presentation with accessibility/tagging in mind

If I revisit slide creation for accessibility in the future, this is likely where I would start rather than with beamer.

### Adobe Acrobat and post-processing

Another possible route is post-processing PDFs in Adobe Acrobat:

- <a href="https://helpx.adobe.com/acrobat/using/create-verify-pdf-accessibility.html">Creating accessible PDFs in Adobe Acrobat</a>

I am less familiar with this, particularly for documents containing substantial mathematics, so I list it here mainly as a possible remediation tool rather than a method I can yet recommend from experience.

---

## 2. Moving beyond PDF-first output

The second branch is to treat LaTeX as source material that can be transformed into formats that are often more accessible by default, especially for web delivery, reflow on variable screen sizes, and integration with modern reading tools.

For me, this may eventually become the preferred long-term direction: writing notes in LaTeX, then publishing them as a website or another web-friendly format.

### Tools and platforms worth watching

- <a href="https://pandoc.org/MANUAL.html">Pandoc User's Guide</a> -- a general-purpose document converter that can bridge LaTeX into many output formats
- <a href="https://pretextbook.org/">PreTeXt</a> -- a "write once, read anywhere" authoring system especially attractive for technical and mathematical content
- <a href="https://latexml.mathweb.org/">LaTeXML</a> -- a LaTeX-to-XML/HTML/MathML converter

### Why this direction is attractive

A web-first or output-agnostic approach can make it easier to support:

- screen readers
- variable screen sizes
- high-contrast or custom display settings
- web publication
- alternate export formats such as HTML, EPUB, or notebooks

I personally have been converting course notes into a GitHub-hosted website rather than distributing PDF alone.

### AI-assisted conversion

I have also had some success using AI tools, including ChatGPT and Gemini, to help convert LaTeX source into HTML or Markdown-compatible content for one-off use cases. I do **not** view this as a substitute for stable methods such as PreTeXt, Pandoc, or LaTeXML. But for limited conversions, draft web pages, or restructuring notes into more flexible formats, it can be quite helpful.

---

## My current perspective

At the moment, I think both branches are worth tracking:

- **Tagged PDF in LaTeX** is becoming increasingly practical and may fit best for documents that must remain close to traditional academic PDFs.
- **Web-first / output-agnostic publishing** may ultimately be the more flexible and more accessible long-term strategy for teaching materials, especially for mathematics-heavy notes.

Because this area is changing quickly, I expect many of the tools and recommendations above to improve over time. At the moment, none of these are a **silver bullet** approach and requires significant heavy-lifting from faculty often with limited direct institutional support. I'm mostly seeing lots of workshops and faculty-led resources being generated.

Just a quick glance at the discourse surrounding this does not paint a rosey picture:

- [Accessibility Real Talk](https://www.reddit.com/r/Professors/comments/1qykci5/accessibility_real_talk/)
- [New Federal Accessibility Requirements](https://www.reddit.com/r/Professors/comments/1qcqf6v/new_federal_accessibility_requirements/)
- [Title II Accessibility Thoughts](https://www.reddit.com/r/Professors/comments/1px0jxw/title_ii_accessibility_thoughts/)
- [New ADA Law Forces Professors to Take Down Their Notes](https://www.reddit.com/r/math/comments/1ryh7md/new_ada_law_forces_professors_to_take_down_their/)

There's a big risk these requirements *degrade* our current instructional materials for students and push us further into just using big publisher materials rather than bespoke content which uses our unique expertise. To quote a commonn response:

> Instructors at my school are responding to this largely by just not posting notes anymore. One writes all of his notes and mark down and then posts them, which seems like a lot of work.

My hope is the tools get up to speed so that going forward, it is a smooth process to make new materials compliant and better for students. If you have built your own accessible LaTeX tools, conversion pipelines, or public teaching materials, I would be glad to hear about them. This is a rapidly changing topics, and community-shared examples are often the most useful way to learn what is working in practice. 

Special thanks to Dr. Hunter Lehmann, Director of Undergraduate Advising for the School of Math at Georgia Tech. Several of the most useful resources collected here were prepared by him, whose guides and workshop materials have been especially helpful for understanding the current state of accessible LaTeX.

---
