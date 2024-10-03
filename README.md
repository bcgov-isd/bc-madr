# BC-MADR

Home repository defining BC Gov's (new) ADR standards.

## What's an ADR?

[*Architectural Decision Records*](https://adr.github.io/), or ADRs, are a way of capturing the what/why/why nots of any particular architectural decision made for a project.

More inclusively, ADRs can also be *Any Decision Record*—and this proposed standard intends to adhere to this as much as possible:

- Why did you choose to use React Native?

- Why doesn't the app sync every 30 minutes?

- Do you need middleware upstream?

- Do we use different colours for dev/test/prod builds? Why does the dev build use pink?

## What is BC-MADR?

BC-MADR is a proposed standard of documenting significant decisions about the direction of any project (with a focus on software development projects).

It's an opinionated extension of [MADR](https://adr.github.io/madr/), with an exceptionally imaginative name.

## Why use this?

What we hope to achieve with BC-MADR is a standardized and predictable way to create and store relevant information about why decisions were made for any project that uses them, rather than fishing through cloud storage to find a Word doc.

There aren't many specific documentation standards that are well known, so documentation across projects is typically created from scratch every time. It'll have a different structure, or will be organized differently, and needs to be learned anew in each instance.

If it isn't deliberately organized in a proper documentation system, chances are high that it'll get lost—or worse, won't be easily discoverable after is *is* lost.

## Do I need to use this?

No. This isn't enforced by anyone.

## How will this repository be used?

This repository is meant to define and host publicly-available BC-MADR specifications and templates. Comments and discussion and welcome, encouraged, and requested from anyone.

## Get started with BC-MADR

If you want to hit the ground running, make a copy of [bc-madr-template.md](bc-madr-template.md) from the `main` branch and start writing!

The template includes comments with directions on how to fill the sections out.

If you want exhaustive information about how BC-MADRs should be created and organized, and the template itself doesn't contain enough info, read the [bc-madr-specification.md](bc-madr-specification.md) additional context.

## I have a suggestion!

Fantastic! Open a GitHub discussion about what you're thinking and let's chat.

## Special thanks

- [adr.github.io](https://adr.github.io/) for compiling ADR information and for igniting the spark for this journey
- [Markdown Architectural Decision Records (MADR)](https://github.com/adr/madr) for their effort in creating and refining the ADR template this repo adapts