# Document Metadata Template

> **Document:** `07-reference/DOCUMENT-METADATA-TEMPLATE.md`  
> **Title:** Document Metadata Template  
> **Version:** 0.1  
> **Status:** Template  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

Every public STATE Markdown page shall expose visible metadata.

## Required header pattern

```markdown
> **Document:** `path/to/file.md`
> **Title:** Page Title
> **Version:** <document-version>
> **Status:** <document-status>
> **Development state:** <optional development or transition state>
> **Created:** YYYY-MM-DD
> **Last modified:** YYYY-MM-DD
> **Author:** Author Name
> **Co-authors:** Names or None
```

`Development state` is optional. When present, it shall appear immediately after `Status`.

## Closed document-status vocabulary

The `Status` field shall use exactly one of the following values:

- `Normative Specification`
- `Reference`
- `Current Documentation`
- `Historical Superseded Specification`
- `Template`

A development or transition state such as `Candidate` is not a document Status. Where such a state is required, it shall be represented separately through `Development state`.

## Field-order rule

Visible header metadata shall use the field order shown above. The optional `Development state` field does not change the order of the remaining required fields.

## Header/footer version integrity

The visible header `Version` value and footer `Version` value shall be identical within the same document.

## Whitespace rule

Metadata shall use consistent Markdown spacing. Tabs are not permitted in metadata. Trailing spaces shall be absent except where exactly two spaces are intentionally used for a Markdown hard break.

## Required footer pattern

```markdown
---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0
Version: <version>
Initial publication: <YYYY-MM-DD>
Last modified: <YYYY-MM-DD>
```

## Publication rule

Metadata is part of the visible publication and shall not be hidden exclusively in front matter, Git history or repository metadata.

Git history complements the page metadata; it does not replace it.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.1  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
