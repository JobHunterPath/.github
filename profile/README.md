# JobHunterPath

Open source job hunting automation.

## What we build

**[job-hunter-core](https://github.com/JobHunterPath/job-hunter-core)** — the automation engine. Scrapes jobs from 15+ sources (ATS APIs, job boards, AI search), scores them with an LLM, and tailors your resume and cover letter.

**[job-hunter-template](https://github.com/JobHunterPath/job-hunter-template)** — template repo with which you can create your personal config repo. Fill in your resume and preferences, GitHub Actions runs the engine for you.
## How it works

    job-hunter-template (your fork)
        config/          your search rules, scoring, LLM provider
        context/         your resume (.tex) and STAR story bank
             │
             ▼  GitHub Actions
    ghcr.io/jobhunterpath/job-hunter-core
        scrape → deduplicate → score (LLM) → tailor → PDF
             │
             ▼
        outputs/         tailored resume + cover letter

## Get started

1. Click **[Use this template](https://github.com/JobHunterPath/job-hunter-template)** on job-hunter-template
2. Add your LLM API key as a GitHub secret
3. Fill in your resume and job search config
4. Run the workflow

## Contributing

See [CONTRIBUTING.md](https://github.com/JobHunterPath/job-hunter-core/blob/main/CONTRIBUTING.md) in job-hunter-core.
