# Data export reliability and recovery
## Observed failure
The initiative founder reports repeated account-export download interruptions near 2.4 GB, with successful resume in Brave. This is a first-person report; it was not independently reproduced, and the root cause and server responsibility are not established.

This is separate from a November 18, 2026 community report of an approximately 4.25 GB export recovered with authenticated HTTP range requests ([E05](../evidence/SOURCE_REGISTER_DRAFT.md)). The community report's author also states that the cause is unknown. OpenAI's current [export guide](https://help.openai.com/en/articles/7260999-exporting-your-chatgpt-history-and-data) documents support steps for stopped or apparently incomplete downloads but does not document a resume/range capability. These reports must not be merged into one incident or used to infer a shared cause.
## Separate browser backup report
A [community post (E14)](https://www.reddit.com/r/ChatGPTcomplaints/comments/1tb905l/) reports missing sections in clipboard copies and browser-generated PDFs of long threads. User-supplied screenshots were reviewed on 25 November 2026; direct retrieval and the exact posting date remain unverified. Later comments report that Firefox can also be affected. This is not evidence of incomplete account ZIP archives or lost server-side data. See [source register](../evidence/SOURCE_REGISTER_DRAFT.md).

## Requested changes
- Resumable authenticated downloads with stable object identity, range support and clear expiry handling.
- Individual conversation and project exports, plus incremental exports.
- Manifest with object lengths, checksums, schema version and completeness indicators; warn if browser-based capture is incomplete and provide a native per-thread export.
- Actionable diagnostics and retry recovery without regenerating the complete archive.
## Acceptance tests
Interrupt a multi-gigabyte download, resume, and verify byte-for-byte integrity against the manifest. Test expired links, changed export identity and interrupted network connections. Verify selective/delta exports against the source dataset. Do not silently omit records. For a long test conversation with unique first, middle, later and final markers, compare native selective export against the authoritative message set, and explicitly report any missing items or incomplete browser capture. A marker check alone is not a complete integrity proof.
## Community participation
Report size, actual bytes received, client, date, error and resume outcome. Remove signed URLs, credentials and private contents.
