---
layout: post
title:  "My Mission: Make Software Less Gullible"
date:   2022-11-09 15:00:00 +1300
categories: blog
tags:   "software vulnerabilities" "program analysis" "program hardening"
---
I once heard advice to graduate students in computer science that it is
important to be able to explain your research to a lay person.  Graduate school
(indeed, life) can be lonely and so many important people in your life may not
be able to understand your work.  The ability to share your work with loved ones
enriches your relationships, your support structure, and your life.

While I immediately believed the wisdom of this advice, I have not always
followed it!  I once started to explain my work to a friend by asking
asking, "well, you know how PDF can be malicious?" and watched as her
eyes widened to saucers and she asked in horror, "PDFs can be malicious?!"

For the sake of that friend as so many others, let me start again.

My career has focused on making software less gullible.  Most software
applications read and interpret some kind of data for you.  For example, a PDF
reader (like Acrobat Reader) will read and display a PDF document for you.  A
normal PDF file tells the reader the words in the PDF, what fonts to use, and
how to lay out the text.

Unfortunately, software is often imperfect and sometimes applications can be
tricked.  When an application has a flaw that allows it to be tricked, we say it
has a /vulnerability/.  Software vulnerabilities make software /gullible/.  Just
as a conman might fool a gullible person into doing something they shouldn't, a
hacker can make vulnerable software do things it shouldn't.

Let's imagine our hypothetical PDF reader has a vulnerability.  A hacker might
craft a file that looks like a PDF, but instead of (or in addition to)
information on the fonts, text, pictures, layout, etc., it has data that
exploits the vulnerability and gets the reader to do other things that are
unrelated to displaying a document.  Unfortunately, when software gets fooled,
it can get fooled *hard*.  Given a sufficiently dangerous vulnerability, a
hacker might have our PDF reader doing things it has no business doing, like
installing backdoors to our computer or running ransomware.

So, yes, PDFs can be malicious.  Images (gifs, jpegs) can be malicious.  Movie
files (mpegs, AVIs, MOVs) can be malicious.  Software vulnerabilities are
entirely too common.

As stated above, much of my research focused on making software less gullible,
that is, less vulnerable to expoilt by malicious inputs (images, movies,
documents, etc.).  I developed tools to find software vulnerabilities.  Human's
have common cognitive biases and psychological foibles that conmen prey upon.
Similarly, there are patterns to many of the software vulnerabilities that
hackers exploit.  I developed tools to detect those patterns so they could be
reported and addressed by software developers.

I also developed tools to /harden/ software against exploit.  As a human, you
may have gone through training to help you recognize email scams, also known as
/phishing attacks/.  You may use tools that attempt to flag and warn you about
phishy emails or prevent you from risky behavior, like sending a social security
number in an email.  Such tools and training make you a harder target for
conmen. I built tools to modify software to make it harder to trick.  Sometimes
it is possible to monitor an application as it runs and detect when it is being
tricked.  In those cases, we can intervene and usually prevent the worst
results.

I worked on tools that help software developers by analyzing the /source code/
that they compile into their application.  More often, I worked on tools that
analyze the software /binaries/, the actual programs that an end user runs.
Analyzing binaries is much more complicated, but it allows us to analyze our
applications when we do not have its source code.  I used /static analysis/,
which analyzes a program without running it and approximates all possible
behaviors of the program.  I also used /dynamic analysis/, which observes a
program as it is run on specific inputs.

I hope to go into more detail on my research in future posts.  I expect I will
usually write at a more technical level, but I hope this post gives a lay person
some insight into what my work is about and what I've hoped to accomplish.
