# Full profile output shape

Return JSON like this. Use `null` for fields not on the page; do not invent data.

```json
{
  "url": "https://www.linkedin.com/in/...",
  "name": "", "headline": "", "location": "", "about": "",
  "experience": [
    { "title": "", "company": "", "employment_type": null, "location": null,
      "start": "", "end": "", "description": "", "skills": [] }
  ],
  "education": [
    { "school": "", "degree": null, "field": null, "start": null, "end": null, "description": null }
  ],
  "skills": [""],
  "certifications": [ { "name": "", "issuer": "", "issued": null, "expires": null, "credential_url": null } ],
  "projects": [ { "name": "", "dates": null, "description": "", "url": null } ],
  "languages": [ { "name": "", "proficiency": null } ],
  "other": { "featured": [], "publications": [], "honors": [], "courses": [] }
}
```
