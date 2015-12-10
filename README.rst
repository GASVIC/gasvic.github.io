================================
G&S Society of Victoria web site
================================

Abstract
========

This document proposes to replace the current Joomla-based web site with a flat
file structure built from text files managed through a git repo.

Rationale
=========

PHP, Joomla, and the plugins/components used are major security flaws, and with
no full-time Joomla administrator to stay on top of things, the site has been
compromised multiple times. Putting out brushfires is a poor use of my time;
fixing this permanently would give peace of mind to both the admin and the
Committee, who will no longer need fear the site being overwritten with
unsavory text, as happened once before.

Additionally, this proposal makes "drive-by editing" possible; any reader of
the web site may propose an edit, which will be sent to the admins for merging.

Costs of this proposal - one-off
================================

This change would require some effort. For instance, the archive would not be
automatically carried over; we'd need to import it, which would require some
manual work (albeit script-assisted). This would also be a good opportunity
to do some heavy-duty data cleaning at the human level, eg removing "tickets
are still on sale" from years-ago shows.

There would be no WYSIWYG editor; instead, you have a simple text markup that
looks like its result. For serious formatting changes, this would be something
new to learn, but most people won't need to learn it. If someone proposes a
change with messed-up formatting, the formatting can be fixed by an admin prior
to the change being merged in.

Archive By Decade may not be implemented yet. (?)

Costs of this proposal - on-going
=================================

I (Rosuav) will keep track of drive-by changes; for our regular editors,
changes can still be done via pretty much the same system. Instead of logging
in to Joomla and making a change, you'd log in to GitHub and make a change.

Timing
======

The Society is currently considering rebranding itself as GASVIC or some other.
Whatever actual acronym and name are eventually accepted, this change will be
a good opportunity to revamp the web site.

The Shop
========

Orthogonally to this proposal, we do need a new shop. The current one has a
number of issues; most notably, it depends on capturing credit card details,
saving them offline, and having a human being do the actual charging of cards.
This is a problem because (a) it's manual and has delays, where people expect
web site charging to be instant; (b) it depends on being allowed to charge a
card without knowing its CVV (since we legally can't save them); and (c) it's
pointless extra work and extra chances to get things wrong.

What do we need from the shop?

* Sales of products which we manufacture ourselves (DVDs, mugs, etc)
* Limited-stock items eg back-issues of TTT or show posters
* Drop-shipment of JeeveS CDs
* Non-physical purchases eg membership renewal (new memberships nice but not critical)
* Possibly made-to-order items eg tees, mugs, posters if we want to go that route
* Postage, with pick-up option
* Maybe "cash in person" payment option?? Not practical for all item types.

The shop should ideally be self-maintaining. Someone adds items to it, and the
orders and money get sent to us. It should _definitely_ have no security burden
for the normal case; SSL, card number handling, etc should all be done for us.
