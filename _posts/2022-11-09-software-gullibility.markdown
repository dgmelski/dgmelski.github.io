---
layout: post
title:  "My Mission: Make Software Less Gullible"
---
I once started to explain my work to a friend by asking, "well, you know how PDF
can be malicious?" Her eyes widened to saucers and she asked in horror, "PDFs
can be malicious?!"

For the sake of that friend as so many others, let me start again.  Sometimes,
software can be tricked into doing things it shouldn't.  My career has focused
on making software less gullible.

Most software applications read and interpret some kind of data for you.  For
example, a PDF reader like Acrobat Reader will read and display a PDF document
for you.  A normal PDF file tells the reader the words in the document, what
fonts to use, and how to lay out the text.

Unfortunately, software is often imperfect and sometimes applications can be
tricked.  When an application has a flaw that allows it to be tricked, we say it
has a *vulnerability*.  Software vulnerabilities make software gullible.  Just
as a conman can fool a gullible person into doing something they shouldn't, a
hacker can trick vulnerable software into doing things it shouldn't.

Let's imagine our hypothetical PDF reader has a vulnerability.  A hacker might
craft a file that looks like a PDF, but instead of (or in addition to)
information on fonts, text, pictures, layout, etc., it has data that exploits
the vulnerability and tricks the PDF reader into doing other things that are
unrelated to displaying a document.  Unfortunately, when software gets fooled,
it can get fooled **hard**.  Given a sufficiently dangerous vulnerability, a
hacker might have our PDF reader doing things it has no business doing, like
installing backdoors to our computer or running ransomware.

So, yes, PDFs can be malicious.  Images (gifs, jpegs) can be malicious.  Movie
files (mpegs, AVIs, MOVs) can be malicious.  Software vulnerabilities are
entirely too common.

As stated above, my research has focused on making software less gullible, that
is, less vulnerable to expoilt by malicious inputs (images, movies, documents,
etc.).  I developed tools to find software vulnerabilities.  Human's have common
cognitive biases and psychological foibles that conmen prey upon.  Similarly,
there are patterns to many of the software vulnerabilities that hackers exploit.
I developed tools to detect those patterns so they could be reported to and
addressed by software developers.

I also developed tools to *harden* software against exploit.  As a human, you
may have had training to recognize email scams such as *phishing attacks*.  You
may use tools that attempt to flag and warn you about phishy emails or prevent
you from risky behavior, like sending your social security number in an email.
Such tools and training make you a harder target for conmen. I built tools to
modify software to make it harder to trick.  Sometimes it is possible to monitor
an application as it runs and detect when it is being tricked.  In those cases,
we can intervene and usually prevent the worst results.

My research included a broad range of techniques for automatic program analysis
and transformation.  I worked on tools that help software developers by
analyzing the *source code* that they compile into their application.  More
often, I worked on tools that analyze software *binaries*, the actual programs
that an end user runs.  Analyzing binaries is much more complicated, but it
allows us to analyze our applications even when we do not have source code.  I
used *static analysis*, which analyzes a program without running it and
approximates all possible behaviors of the program.  I also used *dynamic
analysis*, which observes a program as it is run on specific inputs.

I plan to go into more detail on my research in future posts.  I will usually
write at a more technical level, but I hope this post gives a lay person some
insight into what my work is about and what I aimed to accomplish.
