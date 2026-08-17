# Teaser: Where Does This Even Live?

**Source story**: stories/2026-08-16_document-structure-access.md

**Status**: READY TO POST (Publora scheduling FAILED, see below)

**Post type**: Process Insight

---

## Draft

Everyone assumes the hard part of building an ISMS is writing the policies. We thought so too. Once we'd agreed on the documentation language, the plan was simple: start drafting.

That's not what happened. Before a single ISO document existed, we had to answer a question standard guidance never mentions: where do these documents actually live, and who can open them.

We landed on a restricted SharePoint site, not a folder tucked inside a general one, with access limited to specific named people. Inside it, two folders. Draft, where half-finished procedures and redlines get argued over. Final, the approved, audit-ready version.

Here's the part that mattered most. The auditor gets access to Final only. Draft stays internal, full stop. Letting an auditor see work still being negotiated creates more confusion than it solves.

ISO 27001 tells you what documents to produce. It says almost nothing about where they should physically sit or who gets to watch you write them. Decide that before you draft anything, or you'll be reorganizing mid project.

Setting up your ISMS documentation structure right now? DM me, I'd like to compare notes on what you landed on.

#HiddenRealitiesISO #ISO27001 #ISMS #GRC

(1215 characters)

---

## Backup angle ideas

1. The auditor never saw our Draft folder. That wasn't luck, it was a decision we made before writing a single procedure.
2. We picked a documentation language before we'd written a word of ISO documentation. Turned out that was the easy decision.

---

## First comment (POST THIS MANUALLY AS FIRST COMMENT ONCE THE POST GOES LIVE)

More of what I'm building: github -> ibocus.github.io . CISM prep + toolkits -> bocusiqbal.gumroad.com

---

## Publora scheduling result: FAILED

Target schedule: Wednesday 2026-08-19, 8:00 AM Mauritius (2026-08-19T04:00:00.000Z).

The `create-post` call to `https://api.publora.com/api/v1/create-post` failed at the network layer before reaching Publora: this session's outbound egress proxy returned a policy denial.

Proxy status output:

```
"recentRelayFailures": [
  {
    "ts": "2026-08-17T04:19:02.756Z",
    "kind": "connect_rejected",
    "detail": "gateway answered 403 to CONNECT (policy denial or upstream failure)",
    "host": "api.publora.com:443"
  }
]
```

curl exit code: 56 (recv failure, connection rejected by proxy before TLS).

Per this environment's proxy guidance, 403 policy denials on the egress proxy must not be retried or routed around; the correct action is to report the blocked host. `api.publora.com` is not currently allowed by this session's network policy, so the post was NOT scheduled anywhere. It needs to be posted manually, or the environment's egress allow-list needs to include `api.publora.com` before this routine can auto-schedule again.
