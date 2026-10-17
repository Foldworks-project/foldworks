# Foldworks Glossary

This glossary defines canonical product terminology.

Definitions may be refined during product specification, but changes should be
made deliberately because these terms will eventually appear throughout the
application, documentation, database model, API, and user interface.

## Model

The fundamental object represented by Foldworks.

A Model represents a paper model as a conceptual object rather than an
individual file.

A Model may contain multiple Assets and may have identity, metadata,
presentation, build information, relationships, and variants.

## Asset

A file or other stored representation associated with a Model.

Examples may include:

- PDF patterns;
- PDO files;
- instruction booklets;
- image sheets;
- SVG files;
- textures;
- reference images;
- photographs;
- source archives.

An Asset is not normally an independent catalogue record merely because it is
a separate file.

## Library

A principal organizational and tenancy boundary within Foldworks.

A Library contains Models and associated organizational information.

Users may belong to Libraries through membership relationships.

A single-user installation may initially expose only one Library, while future
multi-user installations may contain multiple Libraries.

The precise permissions and tenancy semantics will be defined during product
and architecture specification.

## Collection

An organizational grouping of Models **within a Library**.

A Collection is not the same thing as a Library.

The precise behavior of Collections remains to be specified.

## User

A person with an account in a Foldworks installation.

Users and Libraries are distinct concepts. A User may eventually belong to
one or more Libraries through membership relationships.

Authentication and authorization behavior remains to be specified.

## Designer

A person or entity credited with designing a paper model.

The precise identity, normalization, and relationship model remains to be
specified.

## Publisher

A person or organization responsible for publishing or distributing a paper
model.

A Publisher is conceptually distinct from a Designer, although the same entity
may occupy both roles.

## Category

A structured classification applied to Models.

The relationship between Categories and Tags remains to be specified.

## Tag

A flexible label used to describe or organize Models.

Tag behavior, scope, normalization, and permissions remain to be specified.

## Build

A record concerning the construction of a Model.

A Build may eventually contain status, dates, notes, photographs, or other
information.

The exact Build model remains to be specified.

## Variant

A distinct version or variation of a Model that remains meaningfully related
to another Model or common identity.

The boundary between a Variant, an Asset, and a separate Model remains to be
specified.

## PDO

A Pepakura model file.

PDO support is a progressive enhancement in Foldworks. The existence of a PDO
must never be required for a Model to receive a first-class experience.