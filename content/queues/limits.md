---
pcx_content_type: concept
title: Limits
weight: 9
meta:
  title: Cloudflare Queues - Limits
---

# Limits

{{<Aside type="note">}}

Many of these limits will increase during the Public Beta of Queues. If you have questions about a certain limit, please [reach out](mailto:queues@cloudflare.com).

{{</Aside>}}

{{<table-wrap>}}

| Feature                                 | Limit                             |
| --------------------------------------- | --------------------------------- |
| Queues                                  | 100 per account <sup>1</sup>      |
| Maximum message size                    | 128 KB                            |
| Maximum message retries                 | 100                               |
| Maximum batch size                      | 100 messages                      |
| Maximum batch wait time                 | 30 seconds                        |
| Maximum message throughput <sup>2</sup> | 100 messages per second           |
| Maximum retention period                | 4 days (96 hours)                 |

{{</table-wrap>}}

<sup>1</sup> This can be raised on request for Enterprise & Workers for Platforms customers. Please [submit a limit increase request](https://docs.google.com/forms/u/1/d/e/1FAIpQLSd_fwAVOboH9SlutMonzbhCxuuuOmiU1L_I5O2CFbXf_XXMRg/viewform).
<sup>2</sup> This is a limit that we will increase, and aspire to effectively eliminate in the future.


Notes:

* 1 KB is measured as 1000 bytes. Messages can include up to ~100 bytes of internal metadata that counts towards total message limits.
* Messages in a queue that have not been consumed after four (4) days are deleted from the queue. Queues does _not_ delete messages in the same queue that have not reached this limit.
