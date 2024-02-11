---
title: Something Better Than Errata
abbrev: Better Than Errata
docname: draft-farrell-errata-00
date: 2024-02-11

# stand_alone: true

ipr: trust200902
area: General
stream: editorial
wg: Network Working Group
kw: Internet-Draft
cat: info

coding: us-ascii
pi:
  toc: yes
  sortrefs:   # defaults to yes
  symrefs: yes

author:
      -
        ins: S. Farrell
        name: Stephen Farrell
        org: Trinity College Dublin
        street: College Green
        city: Dublin
        country: Ireland
        email: stephen.farrell@cs.tcd.ie

normative:

--- abstract

This document outlines some ideas for a system that would
(in the author's view) be better than current errata handling.
This is for discussion and is not expected to become an RFC.


--- middle

# Introduction        {#intro}

Current handling of errata for RFCs is a pain, for all concerned, and is also
fairly ineffective in terms of soliciting comment on RFCs, arriving at new text
when errors are discovered, likely to see many errata not be processed or be
processed at glacial speed, and the current system is also terrible at making
changes visible to RFC readers. It's basically a mess.

In this draft, we sugggest an alternative way of handling the discussion and
dispositon of errors in RFC text. We maintain the idea that this system aims
only to correct errors in RFC text, but is not indended to provide a new route
for revision of RFCs. 

For simplicity, we describe the system as if it existed. We make no real effort
to determine if putting such a system in place would be very easy or very hard
and expensive. We also describe the system as if everyone reads RFCs via the
datatracker.

The author is not invested in the details here, anything approximating what's
described here would probably be fine.

# The New System

Once an RFC is published, then, on the datatracker web page for viewing that
RFC, there will be a "comment/discuss" button that allows readers with a
datatracker account to submit comments on, or questions about, that RFC.
Threaded discussions on comments can follow, not unlike issue discussion on
github.

Discussion threads for RFCs can be browsed/searched.

Discussion threads are expected to be re-directed to an IETF mailing list as
warranted. Discussions can be closed if warranted, e.g. as off-topic. A set of
users will have relevant powers, probably including some new role(s) specifically
for managing such discussions where nobody else might notice, e.g. on some
ancient RFC.

By default, RFC authors and relevant WG chairs will recieve notification
when new discussion threads are started.

Comments can be labelled in various ways, by the original poster or by other
users with additional privileges, e.g. authors, (former) WG chairs, ADs or IRSG members.
The set of priviliges associated with this system are expected to change
slowly over time and are documented at TBD.

One way to label a specific comment that contains a suggested change is as an
erratum.

Comments labelled as errata can be upvoted or downvoted.  Voting power can vary
depending on the user, with authors of the RFC in question, (former) WG chairs,
ADs, etc having more voting power. The set of up/down voting rules are expected
to change slowly over time and are documented at TBD.

Once a comment labelled as an erratum has sufficient upvotes, then it can be
approved by a relevant approver. For the IETF stream any AD can mark a sufficiently
upvogted erratum
as approved. Two relevant WG chairs can also do so if there is a relevant WG
that is still open or only closed within the previous five years.
If an errata for an IETF stream RFC is erroneously approved then that can be reversed by an AD.

It must be possibly to automatically apply the change resulting from
an erratum before it is approved. The required formatting may change
over time and the current requirements are documented at TBD.

Other streams will define other approval schemes.

The default HTML view of RFCs will be that with errata applied.  The list of
applied errata can be viewed via a button, as can any conversation leading up
to an approval. 

# Handing existing errata

Some of the issues arising in migrating to the new system
include:

- Existing approved errata need to be imported into the new system so
as to be displayed as if they had been approved. 

- No action is required with respect to current, posted but unprocessed, errata.
If any of those are really useful, they'll be remembered or re-discovered.  The
expectation is that discussions using the new system will be started for some
of these unprocessed errata and that that will prove to be an easier way to
finally process the actually useful subset of those.

The current errata system should remain available in read-only 
mode so that editors revising RFCs can access e.g. relevant HDFU errata.

# IANA Considerations

This document makes no request of IANA.

# Security Considerations

Spam comments and flamewars could distract and damage the reputation of
the RFC series.

# Acknowledgements

TBD

--- back

# Change Log

## Draft-00 to -01

- TBD


