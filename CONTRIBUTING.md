# Contributing to For the Love of Markdown

Thank you for your interest in contributing to this project. This guide explains how to submit templates, style guides, gallery examples, and improvements.

## Table of Contents

- [What We Accept](#what-we-accept)
- [What We Don't Accept](#what-we-dont-accept)
- [Contribution Process](#contribution-process)
- [Quality Standards](#quality-standards)
- [Template Submission Guidelines](#template-submission-guidelines)
- [Style Guide Submission Guidelines](#style-guide-submission-guidelines)
- [Gallery Submission Guidelines](#gallery-submission-guidelines)
- [Code of Conduct](#code-of-conduct)

## What We Accept

### Templates

- New README formats for specific project types (CLI tools, libraries, datasets, mobile apps, web services)
- Alternative structures for CONTRIBUTING, CHANGELOG, CODE_OF_CONDUCT, SECURITY, or other standard files
- Multilingual templates (translations and culturally adapted versions)
- Domain-specific templates (scientific computing, data science, game development, embedded systems)
- Templates for emerging platforms or technologies

### Style Guides

- Platform-specific guidance for platforms we haven't covered (Bitbucket, Sourcehut, Gitea, etc.)
- Accessibility improvements and inclusive documentation practices
- Performance considerations (rendering speed, file size optimization)
- Internationalization and localization best practices
- Updates to existing guides based on platform changes

### Gallery Submissions

- Links to excellent, well-documented projects with exceptional Markdown
- Brief explanation (50-150 words) of what makes the documentation exemplary
- Specific techniques worth highlighting
- Analysis of structure, hierarchy, and visual design
- Before/after examples showing documentation improvements

### Creative Collections

- New experimental Markdown techniques
- Artistic uses of Markdown (poetry, visual compositions, interactive narratives)
- Examples from other media (print design, web design, graphic design) adapted to Markdown
- Cross-platform compatibility research
- Conversion workflows and tooling recommendations

### Bug Reports and Improvements

- Corrections to existing content
- Broken links or outdated information
- Typos and grammatical errors
- Clarifications and additional examples
- Cross-platform compatibility issues

## What We Don't Accept

- Advertisements or promotional content without educational value
- Duplicate content (check existing guides and templates first)
- Low-effort submissions without explanation or context
- Content that violates licensing or copyright
- Malicious code or security vulnerabilities
- Content promoting discrimination or harassment

## Contribution Process

### Option 1: Direct Edit (Small Changes)

For typos, clarifications, or minor additions:

1. Navigate to the file you want to edit on GitHub
2. Click the pencil icon (Edit this file)
3. Make your changes in the editor
4. Scroll to "Commit changes" section
5. Provide a clear, descriptive commit message
6. Select "Create a new branch for this commit and start a pull request"
7. Click "Propose changes"
8. Add additional context in the pull request description
9. Submit the pull request

### Option 2: Fork and Pull Request (New Content)

For new templates, guides, or substantial additions:

1. Fork the repository to your GitHub account
2. Clone your fork locally: `git clone https://github.com/YOUR-USERNAME/for-the-love-of-markdown.git`
3. Create a new branch: `git checkout -b feature/your-contribution-name`
4. Add your content following the directory structure
5. Test your Markdown across multiple platforms (GitHub, GitLab, VS Code, terminal viewers)
6. Commit your changes: `git commit -m "Add: Brief description of your contribution"`
7. Push to your fork: `git push origin feature/your-contribution-name`
8. Open a pull request from your fork to the main repository
9. Fill out the pull request template with detailed information

### Option 3: Issue Discussion (Larger Changes)

For significant additions or structural changes:

1. Open an issue describing your proposed contribution
2. Wait for feedback from maintainers
3. Discuss approach and implementation details
4. Once approved, follow Option 2 process

## Quality Standards

All contributions must meet these standards:

### Markdown Formatting

- Valid CommonMark or GitHub Flavored Markdown syntax
- Consistent heading hierarchy (no skipped levels)
- Proper use of code blocks with language specification
- Descriptive link text (avoid "click here" or bare URLs in prose)
- Alt text for all images
- Proper list formatting (consistent bullets, proper nesting)

### Content Quality

- Clear, concise writing in standard English
- Proper grammar, spelling, and punctuation
- Logical organization and flow
- Concrete examples demonstrating concepts
- Citations for external sources or references
- No assumptions about reader's background (or clearly stated prerequisites)

### Technical Accuracy

- Tested across multiple Markdown renderers
- Verified links (no dead links)
- Accurate technical information
- Up-to-date with current platform features
- Cross-platform compatibility notes where relevant

### Documentation Standards

- Each template includes three variants (minimal, standard, comprehensive)
- Inline comments explaining each section
- Usage examples with realistic content
- Variations for different use cases
- List of platforms tested

## Template Submission Guidelines

When submitting a new template:

### Required Elements

1. File location: Place in appropriate subdirectory of `/templates/`
2. Naming: Use lowercase with hyphens (e.g., `scientific-computing-readme.md`)
3. Header: Include title and brief description
4. Three variants: Minimal, standard, comprehensive
5. Comments: Annotate each section with purpose and guidance
6. Examples: Include filled-in example with realistic content
7. Metadata: List intended use cases and tested platforms

### Template Structure
```
# Template Name

Brief description of purpose and intended use.

## Intended For

- Project type 1
- Project type 2
- Use case 3

## Variants Included

- Minimal: [description]
- Standard: [description]
- Comprehensive: [description]

## Tested On

- GitHub
- GitLab
- Bitbucket
- VS Code Preview
- Terminal viewers (cat, less, bat)

---

[Minimal variant]

---

[Standard variant]

---

[Comprehensive variant]
```

### Best Practices

- Focus on common use cases first
- Provide clear guidance in comments
- Use realistic example content
- Consider internationalization needs
- Test across multiple platforms
- Include accessibility considerations

## Style Guide Submission Guidelines

When submitting a style guide:

### Required Elements

1. File location: Place in `/style-guides/` directory
2. Naming: Descriptive, lowercase with hyphens
3. Clear scope: Define what the guide covers
4. Principles section: Core recommendations
5. Examples: Good and problematic patterns
6. Checklist: Self-review items
7. References: Links to official documentation

### Style Guide Structure
```
# Style Guide Name

Brief description of scope and purpose.

## Scope

What this guide covers and doesn't cover.

## Principles

Core recommendations and philosophy.

## Guidelines

### Section 1

Detailed guidance with examples.

Good example:
[...]

Problematic example:
[...]

## Checklist

- [ ] Criterion 1
- [ ] Criterion 2

## Platform Considerations

Specific behaviors on different platforms.

## References

- Official documentation
- Related resources
```

## Gallery Submission Guidelines

When submitting a gallery example:

### Required Information

1. Project name and link
2. License information (ensure permissive license allows inclusion)
3. What makes it exemplary (50-150 words)
4. Specific techniques to highlight
5. Screenshots or key excerpts (with permission)
6. Author/maintainer attribution

### Submission Format
```
## Project Name

Link: [URL]
License: [License type]
Submitted by: [Your GitHub username]
Date: [YYYY-MM-DD]

### What Makes It Exemplary

[50-150 word explanation]

### Techniques Highlighted

- Technique 1: [brief explanation]
- Technique 2: [brief explanation]

### Key Excerpts

[Include relevant excerpts or link to specific sections]

### Analysis

[Optional: deeper analysis of structure, hierarchy, visual design]
```

### Criteria for Gallery Inclusion

- High-quality, professional documentation
- Excellent use of Markdown features
- Clear hierarchy and structure
- Strong visual design and readability
- Innovative techniques or approaches
- Accessibility considerations
- Active, maintained project (preferably)

## Code of Conduct

### Our Standards

- Be respectful and considerate in all interactions
- Welcome newcomers and help them learn
- Give constructive feedback
- Accept constructive criticism gracefully
- Focus on what's best for the community and project

### Unacceptable Behavior

- Harassment or discriminatory language
- Personal attacks or trolling
- Publishing others' private information
- Other conduct inappropriate in a professional setting

### Enforcement

Violations may result in temporary or permanent ban from contributing. Report issues to the maintainer.

## Questions and Support

- Open an issue for questions about contributing
- Tag issues with appropriate labels (question, enhancement, bug)
- Be patient waiting for responses (this is a volunteer project)
- Check existing issues before opening new ones

## Recognition

Contributors are recognized in:
- Pull request acknowledgments
- Project documentation
- Release notes (for significant contributions)

Thank you for helping make Markdown documentation better for everyone.

---

Last updated: 2025-11-19
Maintainer: @Querulantenkind
Maintainer: @Querulantenkind
