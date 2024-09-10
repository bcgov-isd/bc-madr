# BC-MADR Specification 0.1

## 1.1 Terminology 

Any references to "template" refers to the BC-MADR template created by this specification.

## 1.2 Requirements language

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "NOT RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in BCP 14 [RFC2119](https://www.rfc-editor.org/info/rfc2119) [RFC8174](https://www.rfc-editor.org/info/rfc8174) when, and only when, they appear in all capitals, as shown here.

## 2. Pillars of BC-MADRs

BC-MADRs and their supporting systems MUST fulfill several fundamental pillars:

### 2.1 Storage and proximity

1. For any project (source code or otherwise), BC-MADRs MUST be stored in a git repository.

2. If a project is software development, BC-MADRs MUST be stored in the same repository as the source code.

3. In a repository, BC-MADRs MUST be stored at the following path and nowhere else:

	`<repo_root>/docs/decisions`

	⚠TBD: Should we allow decision subfolders or require all decisions be kept in the same folder?

4. When naming BC-MADR files, you are:

	- REQUIRED to use kebab-naming. (`this-is-kebab-naming`)

	- REQUIRED to save as a Markdown file. (`this-is-kebab-naming.md`)

	- REQUIRED Use an incremental scheme in the filename.

	- RECOMMENDED to use an integer auto-increment scheme, e.g.

		```bash
		0001-this-is-kebab-naming.md
		0002-this-is-more-kebab-naming.md
		0003-this-is-additional-kebab-naming.md
		```
		
		Alternatively, you can use whatever incremental scheme that fits best for your project, but: when the filenames are sorted in ascending order, the list of BC-MADRs MUST be ordered from oldest to newest.

	- RECOMMENDED to write the same title as in the file itself, so it is easier to find decisions. Example:

		`0001-use-the-bc-madr-decision-format-in-bc-gov.md`:

		```markdown
		[//]: # (v0.1 bc-madr)

		# Use the BC-MADR decision format in BC Gov

		...
		```

### 2.2 "Lower" friction

⚠Coming soon

### 2.3 Dedicated and decoupled history

A given set of BC-MADRs MUST only belong to a single project in order to maintain a single source of truth.

All significant decisions made for a project's technical direction MUST be recorded in a BC-MADR.

BC-MADRs MUST NOT contain direct references to the project's source code, as these references are not enforced by tools like compilers. 

BC-MADRs MAY contain code examples if they are relevant to a decision and are not intended as a direct reference to project source code.

#### 2.3.1 Significant decisions

If the answer to any of the following questions is "Yes," create an ADR to record the decision.

- Does this decision affect or change the architecture of the project?

	- Integrating with APIs, databases, platforms, etc.

- Do I need to make a pros/cons list for this decision?

- Does this decision affect the User Experience (UX) of the project?

	- Adding, changing, or removing features

	- Cosmetic changes

- Am I implementing a feature with logic that is not obvious to a user?

- If someone asks "why" about a decision related to the project, does it require deep understanding of that project?

#### 2.3.2 Technical direction

⚠TBD: Should BC-MADRs be used only for technical decisions, or also include operational decisions?

#### 2.3.3 Contents of a BC-MADR

A single BC-MADR MUST, at a minimum, contain information about:

##### 2.3.3.1 What is being decided

A short description (approximately less than ~12 words) of the the driving reason for the decision being made MUST be written as the main title of the BC-MADR.

⚠TBD: What should our maximum word limit for a short description be? If we should even have a limit at all?

##### 2.3.3.2 Who is / are making the decision

BC-MADRs MUST be attributed to individuals or groups of people by their full names, in a comma-separated list, in last-name alphabetical order.

BC-MADRs MAY also include the name of the project's team.

##### 2.3.3.3 The decision outcome

BC-MADRs MUST include what was ultimately chosen.

BC-MADRs MUST also include contextual information about other options that were considered and not chosen. If no other options were considered, it MUST be explicitly written that "No other options were considered."

##### 2.3.3.4 Potential negative consequences

BC-MADRs MUST include any potential negative consequences of a decision: any pitfalls, gotchas, deficiencies that must be dealt with or worked around, or other such issues.

Note: it is acceptable to choose an option with issues as long as its positive consequences are worth it, and is approved by all relevant stakeholders.

##### 2.3.3.5 What is the status of the decision

A BC-MADR must have one of the following statuses:

- Draft
- Proposed
- Rejected
- Accepted
- Deprecated
- Superseded by [xyz](iiii-xyz.md)

⚠TODO: Go into detail about what each status means and when they apply

##### 2.3.3.6 When was the decision approved and finalized

A BC-MADR MUST be considered valid and active when it has gone through review with relevant project stakeholders who have all given their explicit approval to change its Status to "Accepted."

### 2.4 Accessibility

It is recommended to deploy versioned copies of BC-MADRs in a more human-consumable form to any number of destinations, but the original files themselves MUST be kept according to Section 2.1.

## 3. Tooling

⚠Coming soon

## 4. Versioning

### 4.1 The specification

⚠TBD: Please discuss!

### 4.2 Templates

1. Templates MUST be versioned the same as their specifications.

2. The version of a template MUST be written in the first line of a file.

3. The version of a template MUST be the only content in the first line of a file.

4. The version MUST be written in the form:

	`[//]: # (v<version here> bc-madr)`

	Example:

	`[//]: # (v0.1 bc-madr)`

5. The version line is NOT REQUIRED to have an empty line below it.
