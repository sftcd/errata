---
title: Something Better Than Errata
abbrev: Better Than Errata
docname: draft-farrell-errata-01
date: 2024-12-18

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
    RPCTBD:
        title: somewhere the RPC publish stuff
        date: 2024
        author:
            org: RPC

--- abstract

This document outlines some ideas for a new errata handling policy
that would (in the author's view) be better than current errata handling.
This is for discussion and is not expected to become an RFC.


--- middle

# Introduction        {#intro}

Current handling of errata for RFCs is a pain, for all concerned, and is also
fairly ineffective in terms of soliciting comment on RFCs, arriving at new text
when errors are discovered, likely to see many errata not be processed or be
processed at glacial speed, and the current system is also terrible at making
changes visible to RFC readers. It's basically a mess.

In this draft, we set out some ideas for a new errata handling policy and,
as an exemplar, sugggest an alternative way of handling the discussion and
dispositon of errors in RFC text. We maintain the idea that this system aims
only to correct errors in RFC text, but is not intended to provide a new route
for revision of RFCs. 

For simplicity, we describe the example system as if it existed. We make no real effort
to determine if putting such a system in place would be very easy or very hard
and expensive. We also describe the example system as if everyone reads RFCs via 
one interface such as that provided by the IETF datatracker.

The author is not invested in the details here, anything approximating what's
described here would probably be fine, e.g.  another draft
{{?I-D.rescorla-rfc-jit}} describes a much broader proposal that includes some
aspects quite similar to those described below.

If useful, comments/issues/PRs are welcome at: https://github.com/sftcd/errata/

# Policy versus Implementation

Many of the details below are provided via indirection, using the {{RPCTBD}},
reference. In those cases, the intent is that the referenced documents are
maintained by, and under the change control of, the RPC, but that those details
MUST ensure that control over the content of RFCs remains with the community
and is never given to the RPC or IETF LLC.  The RPC are expected to consult
with the community as changes are considered.

There is one exception - where user-provided input is allowed, then spam will
follow. The RPC are empowered to delete obvious spam as soon as possible. The
RPC should periodically (perhaps yearly) report to the RSAB on recent trends
related to spam in this system.

# A Possible New System

Once an RFC is published, then, e.g. on the datatracker web page for viewing that
RFC, there will be a "comment/discuss" button that allows readers with a
relevant account to submit comments on, or questions about, that RFC.
Threaded discussions on comments can follow, not unlike issue discussion on
services like github.

Discussion threads for RFCs can be browsed/searched.  Discussion threads are
expected to be re-directed to an IETF mailing list as warranted. Discussions
can be closed if warranted, e.g. as off-topic. A set of users will have
relevant powers, probably including some new role(s) specifically for managing
such discussions where nobody else might notice, e.g.  on some ancient RFC. By
default, RFC authors and relevant WG/RG chairs will recieve notification when
new discussion threads are started.

Each RFC stream may define its own procedure for the relevant privileges
involved; for example, discussion threads on IETF stream documents would be
expected to be redirected to an IETF mailing list at some point, but the "when"
and "how" decision would be made by the IETF, not by the RFC Editor.  By
default, old documents not assigned to a particular stream are treated as if
they were IETF stream, unless another stream manager claims them.

Comments can be labelled in various ways, by the original poster or by other
users with additional privileges, e.g. authors, (former) WG chairs, ADs or IRSG
members.  The set of priviliges associated with this system are expected to
change slowly over time and are documented at {{RPCTBD}} in accordance with
stream-manager policies.

One way to label a specific comment that contains a suggested change is as a
reported erratum.

Comments labelled as reported errata can be upvoted or downvoted.  Voting power
can vary depending on the user, with authors of the RFC in question, (former)
WG chairs, ADs, etc having more voting power. The set of up/down voting rules
are expected to change slowly over time and are documented at {{RPCTBD}}. Note
that the idea of up/down-voting here only applies to discussion threads and is
envisaged to precede (and definitely not replace) stream-specific approval
processes for errata.

Once a comment labelled as an erratum has sufficient upvotes, then it is
brought to the attention of relevant stream-specific approvers, e.g. via a mail
to the relevant approvers, WG or area list. For the IETF stream, any AD can
always mark a sufficiently upvoted erratum as approved. Additional
stream-specific approval mechanisms can also be defiened, e.g. allowing two
relevant WG chairs do so if there is a relevant WG that is still open or only
closed within the previous five years. If an errata for an IETF stream RFC is
erroneously approved then that can be reversed by an AD. Approvers can also
change a discussion thread into a proposed erratum without requiring upvoting.

It must be possible to automatically apply the change resulting from an erratum
before it is approved. The required formatting may change over time and the
current requirements are documented at {{RPCTBD}}.

The typical HTML view of RFCs should be that with errata applied.  The list of
applied errata however do need to be viewable (e.g. via a button), as should 
discussion from the initial report up to and including approval. 

# Handing existing errata

Some of the issues arising in migrating to the new system include:

- Existing approved errata need to be imported into the new system so as to be
  displayed as if they had been approved. 

- One possibility is that no action is required with respect to current, posted
  but unprocessed, errata reports.  The argument for this is that if any of those are
really useful, they'll be remembered or re-discovered.  The expectation is that
discussions using the new system will be started for some of these unprocessed
errata and that that will prove to be an easier way to finally process the
actually useful subset of those.

- Another possibility is to try import existing unprocessed errata reports
into the new system, however the author isn't sure how that might be done
in a useful way (so currently favours the "no action" possibility) but that's
a topic to discuss.

The current errata system should remain available in read-only mode so that
editors revising RFCs can access e.g. relevant HDFU errata.

# IANA Considerations

This document makes no request of IANA.

# Security Considerations

Spam comments and flamewars could distract and damage the reputation of
the RFC series.

# Acknowledgements

Thanks to those on the rfc-interest list for discussion of this topic,
in particular Brian Carpenter, for specific comments on the text.

All bad ideas, errors and omissions of course remain the fault of the
author.

--- back

# Change Log

## Draft-00 to -01

- Incorporated feedback from rfc-interest list.


