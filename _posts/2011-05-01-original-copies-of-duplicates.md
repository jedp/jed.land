---
layout: post
title: Original Copies of Duplicates
date: 2011-05-01
---

Digging through boxes of ancient junk, I just unearthed a collection of book
return receipts from Doe Library at UC Berkeley. This brings back memories of a
fun hack and an ironic lesson in the problem of authenticity and forgery.

I was a graduate student at Berkeley, working towards a doctorate in Latin
(Ph.D. 2001 w00t). As a graduate student, I read, or pretended to read, lots of
books. And when you return a book to the UC Berkeley library, there was a not
infinitesimal chance that they would misplace the book and tell you you'd lost
it and would have to pay for it. For a graduate student to pay for anything
is a burden; and "paying for" some rare 19th-century German volume is
inconceivable.

To its credit, the library system acknowledged that it was unreliable and
offered book return receipts. These were slips of paper on which you would
write the call number of the book you were returning, your name, and the date.
The librarian would sign and stamp the receipt as a token that you had indeed
returned the book. That way, when the call came that you had failed to return a
certain volume, you had your proof.

As I said, as a graduate student, I filled out scores of these each week. It
felt like a stupid pointless labor, since they already knew I had the book
checked out. It was in the system. You could look it up on the VT101 terminals!
This is the sort of thing computers are there to automate for you. I thought
they should just be able to print a receipt for me right there with no signing
involved by anyone. But the librarians said they had no such system and This Is
The Way We Do Things.

Hmm. So I wrote a Perl script to dial into the library modem pool and query the
database for information about all the books I had checked out. There was a
little reverse engineering required for the results it sent back. I recall it
was peppered with lots of non-printing characters whose purpose seemed to be to
inject load-bearing pauses or something. I wasn't sure. Pretty quickly, though,
I had something that made sense of the results and extracted the data I needed.

I wrote a PostScript program that would reproduce as exactly as possible the
forms they provided. Here's what one of the originals looked like:

![An manually filled-out receipt](/assets/book-receipt-manual.jpg)

The only important information is the call number and the patron's name. It's
good to have the title and book author there as well in case there's a typo in
your call number, I guess.

I carefully measured this slip, trying to duplicate every detail (including the
way the descenders in the p and y in 'Copy' cross the line of the box).
Unfortunately, on my Linux box (I don't remember what distro I was using in
1999), I did not have all the typefaces they were using, so I used what was
available to me. Here's what I came up with:

![An auto-generated receipt](/assets/book-receipt-generated.jpg)

Awesome, I thought. All that time I would have wasted filling in these forms I
have now spent on something actually interesting. (I notice that these are
receipts for books on metrics, an area of lingistics I find particularly
awesome, in which I did some work when I should have been working on my more
"marketable" dissertation instead. So this is a double transcript of my working
on something I found more captivating than the things I was actually supposed
to be doing.)

But to my surprise, when I presented the librarian with my auto-generated book
return receipts, he did not want to accept them. He complained that they were
not the real thing! That they were false copies of the true item! Furthermore,
he objected that my name was printed by the laser printer, and had not been
written by hand by me. Therefore, in his mind, this was a forgery and could not
be used to prove with authenticity that I had returned the book I was
returning, even if he signed it and stamped the date on it.

I replied that the receipts he wanted me to fill out were themselves copies of
copies (which you could easily tell by the accumulation of photocopier
artifacts). The library's receipts were no closer to some Platonic ideal of a
Book Return Receipt than mine. In fact, you could say they were farther away,
because if anything was being reproduced, it was the data at the heart of the
system. And my approach removed the possibility of human errors in
transcription.

Furthermore, my name, filled in by the computer program so I wouldn't have to
do any writing at all, wasn't replacing a personal signature (and the imprint
of a signature itself is a problematic event, as Derrida can tell you);
instead, like everyone, I wrote my name in block capitals for legibility. The
real transaction in these receipts takes place when the librarian signs and
dates them. That's the whole point.

Well, as you can see from the datestamps on the receipts above, the librarian
eventually conceded to stamp my book as "returned," but not without becoming
frustrated with me and turning the conversation over to his supervisor. I don't
remember much of what she said, but don't think she was so troubled by my copy
of a copy of a copy. And I was able to use my book return receipt generator for
the rest of my time at Berkeley.

I don't know if they still use book return receipts at Berkeley. I'd be
interested to hear from anyone about what they do now. I expect that 12 years
later they can scan the bar code and give you a printed receipt without anyone
signing anything – the physical receipt is what makes the system work – but I
don't know. I also miss those VT101 terminals.

