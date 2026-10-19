# Model and Asset Identity

**Status:** Draft
**Product area:** Core domain model
**Last updated:** 2026-10-19

## Purpose

This document defines the current product understanding of Models, Assets, and
their relationships in Foldworks.

It describes the paper-model domain as Foldworks must understand it.

It does **not** define a database schema, storage architecture, API, class
hierarchy, or implementation strategy.

Where the domain remains ambiguous, this document records that ambiguity
rather than inventing certainty.

---

## 1. The Model is the fundamental catalogue object

Foldworks catalogues **Models, not files**.

A Model represents a paper-model design as the collector understands it.

A Model may be represented or supported by many files, including:

- printable pattern PDFs;
- PDO files;
- instruction documents;
- image sheets;
- SVG files;
- textures;
- cover artwork;
- reference images;
- photographs;
- archives;
- alternate print versions;
- supplementary material;
- other related files.

These files are Assets associated with Models.

The existence of multiple files does not imply the existence of multiple
Models.

Likewise, the existence of only one file does not necessarily mean that the
file has only one purpose or role.

---

## 2. Subject and Model are not the same thing

The thing represented by a paper model is conceptually distinct from the
paper-model design itself.

For example:

```text
Subject:
USS Enterprise NCC-1701-D

Possible Models:
- one designer's Enterprise-D papercraft;
- another designer's Enterprise-D papercraft;
- a substantially redesigned or enhanced version;
- other independently useful representations of the same subject.
```

Multiple Models may therefore represent the same subject.

The precise representation of Subject within Foldworks remains to be
specified.

---

## 3. Model identity is inferred from evidence

No single property necessarily determines whether a group of files represents
one Model.

Useful evidence may include:

- directory containment;
- directory names;
- filenames;
- common specimen or subject names;
- designer;
- publisher;
- scale;
- artwork;
- printable geometry;
- part layout;
- file contents;
- original distribution package;
- accompanying instructions;
- associated PDO files;
- other contextual relationships.

For example, a directory named `Enterprise-D` containing several files whose
names also contain `Enterprise-D` provides strong evidence that the files are
related.

That evidence does not by itself establish the final catalogue boundary.

### Principle

> Filesystem structure and naming are evidence of Model identity, not Model
> identity itself.

---

## 4. Design identity matters more than superficial file differences

Different files may represent the same Model.

For example:

```text
Enterprise-D-1-1700.pdf
Enterprise-D-1-2500.pdf
```

If these files contain materially the same paper-model design and differ only
because the same artwork and parts have been scaled for different print sizes,
they may represent variants or printing options of the same Model.

Scale alone therefore does not necessarily establish a distinct Model. However, the collector may still choose to catalogue different scales as
separate Models.

Similarly:

```text
Enterprise-D-white.pdf
Enterprise-D-weathered.pdf
Enterprise-D-Aztec.pdf
```

may represent the same Model when the underlying parts and design are
materially the same and only their appearance differs.

However, differences can become substantial enough that the collector may
reasonably consider the result a different Model.

Examples may include:

- additional parts;
- removed parts;
- substantially altered geometry;
- substantially different construction;
- additional detail intended for a larger scale;
- materially revised artwork;
- combinations of differences that make the design meaningfully distinct.

There is not yet a universal mechanical threshold at which a Variant becomes
a separate Model.

### Principle

> Model identity may depend on the degree and meaning of differences, not
> merely on whether differences exist.

---

## 5. The collector determines catalogue boundaries

Some paper-model relationships do not have one objectively correct catalogue
interpretation.

Consider:

```text
Enterprise-D/
├── Enterprise-D.pdf
├── Enterprise-D.pdo
└── captains_yacht.pdf
```

`captains_yacht.pdf` could represent several different things.

It might contain a small Captain's Yacht intended as a component or companion
piece at the appropriate scale for the Enterprise-D.

It might contain parts that modify the Enterprise-D itself to provide a
docking location for the Captain's Yacht.

It might instead contain a complete standalone Captain's Yacht at 1:200 scale.

In the final case, one collector might choose to catalogue the Captain's Yacht
as part of the Enterprise-D Model while another might reasonably catalogue it
as a separate Model related to the Enterprise-D.

Neither organization is inherently incorrect.

### Principle

> Foldworks may infer relationships, but the collector determines catalogue
> boundaries.

Automatic analysis should therefore make recommendations rather than silently
turn uncertain inferences into authoritative organization.

---

## 6. Relatedness is not necessarily containment

Two Models can be meaningfully related without one being contained by the
other.

A standalone Captain's Yacht Model may, for example, have relationships such
as:

- companion to Enterprise-D;
- intended to be displayed with Enterprise-D;
- distributed with Enterprise-D;
- designed by the same designer;
- associated with an Enterprise-D modification.

This relationship should not require the Captain's Yacht to cease being an
independently catalogued Model.

### Principle

> Catalogue membership and semantic relationship are separate questions.

The precise set of Model-to-Model relationship types remains to be specified.

---

## 7. Variants exist, but their exact representation remains open

Foldworks needs to represent meaningful variations of the same underlying
paper-model design.

Potential Variant dimensions include:

- scale;
- colouring;
- texture;
- weathering;
- language;
- print format;
- detail level;
- other design options.

A difference in one of these attributes does not automatically establish
either a Variant or a distinct Model.

The precise representation of Variants remains to be specified.

In particular, this document does not yet determine whether Variant should be:

- a first-class domain object;
- metadata associated with Assets;
- a relationship between Models;
- some combination of these approaches.

That decision should follow further product specification.

---

## 8. Sets organize Models without destroying Model identity

Foldworks should allow independently useful Models to be associated with a
named Set.

For example:

```text
Star Trek 60th Anniversary Enterprise Set
├── Enterprise-D
├── Enterprise-E
└── Voyager
```

Each member remains an independently catalogued Model.

A Set may provide useful presentation and organizational context, but Set
membership must not require its Models to become subordinate files or lose
their individual identities.

The precise behavior and representation of Sets remains to be specified.

---

## 9. Provenance and user organization are different

The way a creator, designer, publisher, archive, or distributor grouped
material is useful information.

It does not necessarily dictate how the collector must organize that material.

For example, a publisher may officially release:

```text
Star Trek 60th Anniversary Enterprise Set
├── Enterprise-D
├── Enterprise-E
└── Voyager
```

A collector may decide that Voyager does not belong in their personal
Enterprise Set and organize it separately.

Foldworks should be capable of preserving the fact that Voyager was originally
distributed as part of the official Set without forcing the collector to
retain that organization.

The same principle applies to:

- original archive contents;
- directory structure;
- publisher categories;
- designer groupings;
- package names;
- official Sets;
- other provenance information.

### Principles

> Foldworks should preserve provenance without imposing provenance as
> organization.

> User organization may differ from publisher, designer, package, filesystem,
> or inferred organization without destroying those original relationships.

---

## 10. Assets may be associated with more than one Model

An Asset must not be assumed to belong exclusively to one Model.

For example:

```text
Star-Trek-Starships-Instructions.pdf
```

might contain instructions for:

```text
Enterprise-D
Enterprise-E
Voyager
```

Foldworks should be able to store or reference the underlying file once while
making it available from each relevant Model.

Removing one of those Models from a user-created Set must not sever that
Model's independent relationship with the shared instruction Asset.

### Principle

> Relationships between Models and Assets must not depend upon organizational
> groupings such as Sets.

Foldworks should not create unnecessary physical duplicates merely to
represent multiple catalogue relationships.

---

## 11. Model-to-Asset relationships may contain context

The relationship between a Model and an Asset may itself contain useful
information.

For a shared instruction document, for example:

```text
Star-Trek-Starships-Instructions.pdf
│
├── Enterprise-D
│   └── pages 5–11
│
├── Enterprise-E
│   └── pages 12–19
│
└── Voyager
    └── pages 20–27
```

When the user opens the instructions from the Enterprise-D Model, Foldworks
could open the shared document directly at page 5.

Page ranges are one example of relationship context.

Other forms of relationship context may be discovered during further product
specification.

---

## 12. One Asset may serve multiple roles

A single physical file may contain several kinds of useful material.

For example:

```text
Enterprise-D-complete.pdf

Pages 1–3     Cover / information
Pages 4–10    Build instructions
Pages 11–32   Printable model parts
Pages 33–35   Reference photographs
```

Foldworks should not need to physically split this file in order to understand
or present these different roles.

The same Asset may therefore serve roles such as:

- presentation or cover material;
- printable model parts;
- build instructions;
- reference material;
- supplementary information.

Where useful, a role may apply to the entire Asset or to a section of it.

The exact vocabulary and representation of Asset roles remains to be
specified.

---

## 13. Manual structure must not depend on automatic recognition

Automatic recognition of Model boundaries, document sections, Asset roles,
scales, subjects, and relationships would be valuable.

It is not a prerequisite for useful Foldworks functionality.

For example, Foldworks may initially allow a user to specify:

```text
[x] Build instructions are contained within this file
```

More detailed manual organization might allow the user to identify:

```text
Instructions: pages 4–10
Model parts:  pages 11–32
Reference:    pages 33–35
```

Automatic analysis could later propose the same structure for confirmation.

### Principle

> Automation should enrich manual structure, not replace it.

A useful progression is:

```text
Manual → Assisted → Automatic
```

The product should remain functional at every stage.

---

## 14. Ambiguity is a valid state

Foldworks will encounter cases where it cannot reliably determine:

- whether two files represent the same Model;
- whether something is a Variant or a separate Model;
- whether an Asset belongs to one or several Models;
- whether a file is an add-on, companion, modification, or standalone Model;
- what role part of a document serves.

Foldworks must not invent certainty merely to produce a tidy catalogue.

The collector should be able to defer a decision.

### Principle

> "Decide later" is a valid catalogue state.

An unresolved Model should remain browsable and useful while uncertainty
exists.

---

## 15. Reconciliation should be visual

Paper modelling is a highly visual domain.

When Foldworks asks a collector to resolve an ambiguous Model, Asset, Variant,
or relationship, it should provide useful visual evidence whenever practical.

This may include:

- thumbnails;
- pageable document previews;
- side-by-side document comparison;
- page counts;
- filenames;
- detected scale;
- detected subject;
- detected designer or publisher;
- other relevant metadata.

For example, when deciding whether two PDFs are merely different scales of the
same Model or meaningfully different designs, the user should ideally be able
to inspect both documents without leaving the reconciliation workflow.

### Principle

> When Foldworks asks the collector to make a decision about visual material,
> Foldworks should prefer showing the evidence over merely describing the
> evidence.

---

## 16. Files should not be duplicated merely to satisfy catalogue structure

Foldworks' conceptual organization does not need to mirror physical file
organization.

One Asset may:

- serve multiple Models;
- serve multiple roles;
- contain multiple meaningful sections;
- participate in multiple relationships.

Foldworks should therefore avoid unnecessary copying or splitting of files
merely because the catalogue represents them in several places.

This principle does not yet determine Foldworks' storage architecture.

It establishes only the product expectation that conceptual relationships
should not require unnecessary physical duplication.

---

## 17. Current working model

The domain discovered so far is better understood as a network of
relationships than as a strict filesystem-like hierarchy.

Conceptually, Foldworks may need to understand relationships among things such
as:

```text
Subject
Model
Asset
Variant
Set
Designer
Publisher
Collection
User
Library
```

This list does not establish implementation entities or database tables.

Some concepts may ultimately be represented as metadata or relationships
rather than independent objects.

### Principle

> Do not force a naturally relational paper-model collection into an
> unnecessarily rigid tree.

---

## 18. Open questions

The following questions remain deliberately unresolved:

1. What is the precise minimum definition of a Model?
2. Should Subject become a first-class Foldworks concept?
3. What exactly distinguishes a Variant from a separate Model?
4. Should Variant be a first-class object?
5. What Model-to-Model relationship types should Foldworks support?
6. Can a Model belong to multiple Sets?
7. Are official Sets and user-created Sets the same product concept or
   different concepts?
8. What information about original packages and filesystem structure should
   Foldworks preserve as provenance?
9. What Asset roles should Foldworks recognize?
10. How should page ranges and other partial-Asset relationships be represented
    to the user?
11. What happens when an underlying shared Asset is moved, renamed, replaced,
    or deleted?
12. How should Foldworks distinguish a duplicate Asset from an intentionally
    duplicated file?
13. How should Model identity survive filesystem changes?
14. What information may Foldworks infer automatically, and what confidence
    should be required before acting without confirmation?
15. How should unresolved catalogue decisions be surfaced without becoming
    annoying or burdensome?

These questions should be answered through further product specification
before implementation architecture is allowed to answer them accidentally.

---

## 19. Summary of established principles

The following principles are established by the current product discussion:

1. **The Model is the fundamental catalogue object.**
2. **Files are Assets associated with Models.**
3. **Subject and Model are conceptually different.**
4. **Filesystem structure and naming are evidence, not authority.**
5. **Scale differences alone do not necessarily create separate Models; the
   collector may still choose to catalogue different scales separately.**
6. **Appearance differences alone do not necessarily create separate Models.**
7. **The degree and meaning of differences matter to Model identity.**
8. **The collector determines catalogue boundaries when reasonable
   interpretations differ.**
9. **Catalogue membership and semantic relationship are separate questions.**
10. **Variants are meaningful, but their exact representation remains open.**
11. **Sets organize Models without destroying individual Model identity.**
12. **Provenance must be preservable without dictating user organization.**
13. **Assets may be shared among multiple Models.**
14. **Model-to-Asset relationships may contain context such as page ranges.**
15. **One Asset may serve multiple semantic roles.**
16. **Conceptual relationships should not require unnecessary physical file
    duplication.**
17. **Manual organization must remain useful without automatic recognition.**
18. **Automation should progress from manual to assisted to automatic.**
19. **Ambiguity is legitimate, and decisions may be deferred.**
20. **Reconciliation should present visual evidence whenever practical.**
21. **The paper-model domain should not be forced into an unnecessarily rigid
    hierarchy.**