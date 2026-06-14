# Anu Viswan Portfolio Website - Project Instructions

## Overview

This project is a professional portfolio website for Anu Viswan, a Lead Software Architect / Solution Architect / Principal Engineer with over 20 years of experience.

The website is intended to complement a resume and LinkedIn profile by presenting a concise professional narrative, career highlights, selected projects and technical interests.

The website must NOT function as a detailed project repository or expose confidential information from current or former employers.

---

# Primary Goals

The website should communicate:

- Technical leadership
- Solution architecture experience
- Scientific and industrial software expertise
- International collaboration experience
- Long-term career progression
- Thought leadership and technical writing

The website should feel professional, modern and trustworthy.

---

# Technology Stack

- Vue 3
- TypeScript
- Vite
- Vue Router
- Tailwind CSS

No backend is required initially.

The site should be deployable as a static website.

---

# Design Principles

## General Style

- Light theme
- Minimalist design
- Clean typography
- Large whitespace
- Modern but conservative
- No flashy animations
- No dark hero sections
- No personal photograph

The website should feel closer to a professional architect portfolio than a startup landing page.

---

# Navigation

Top-level navigation:

- Home
- About
- Career Highlights
- Writing
- Contact

Resume download button should always be visible.

---

# Reference Files

When prompted to look into reference file, should refer location : /src/data/reference

# Data Source Strategy

All portfolio content should be driven from JSON files.

Pages should never hardcode project details.

---

# Data Structure

## Career Highlights

Location:

/src/data/career.json

Example:

```json
{
  "career": [
    {
      "company": "Calpine Group",
      "period": "2005-2015",
      "title": "Principal Technical Lead",
      "domain": "Scientific & Pharmaceutical Automation"
    }
  ]
}
```

---

## Projects

Location:

/src/data/projects.json

Example:

```json
{
  "projects": [
    {
      "title": "Kruss Instruments",
      "role": "Principal Engineer",
      "period": "2022-Present",
      "domain": "Scientific Instrumentation",
      "summary": "Contributed to software platforms supporting scientific instruments used in surface science and analytical measurement applications.",
      "technologies": ["C#", ".NET", "WPF", "Vue.js", "TypeScript"]
    }
  ]
}
```

Project listing pages should read directly from this file.

Project detail pages should load based on slug.

---

## Skills

Location:

/src/data/skills.json

Categories:

- Architecture
- Leadership
- Platforms
- Languages
- Frameworks
- Databases
- Cloud
- Scientific Technologies

---

# Personal Brand

The website should consistently position Anu as:

Lead Software Architect | Solution Architect | Principal Engineer

Key themes:

- Scientific Instrumentation
- Industrial Automation
- Healthcare Platforms
- Enterprise Systems
- Technical Leadership
- Software Architecture
- Modernization

Avoid positioning as:

- Full Stack Developer
- Frontend Developer
- Backend Developer
- Freelancer

The emphasis should be on architecture, leadership and engineering impact.

---

# Content Priority

When space is limited prioritize:

1. Professional Experience
2. Technical Leadership
3. Scientific / Industrial Expertise
4. Architecture
5. Writing & Community Contributions
6. Personal Projects

The site should feel like the portfolio of a senior architect with 20+ years of experience rather than a showcase of technologies.
