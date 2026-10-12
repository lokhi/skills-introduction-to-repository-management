# Contributing to the Mergington High Extra-Curricular Activities Website

Thank you for helping improve our school's website! Whether you want to add
club activities, fix a bug, or suggest a feature, this guide will help you get
started.

## Development Setup

1. Clone the repository and change into its directory.
2. Create and activate a Python virtual environment:
   ```sh
   python3 -m venv .venv
   source .venv/bin/activate
   ```
   On Windows, use `.venv\Scripts\activate`.
3. Install dependencies: `python -m pip install -r requirements.txt`.
4. Start a local MongoDB server at `mongodb://localhost:27017/`, which is the
   address used by `src/backend/database.py`. GitHub Codespaces also provides
   a prepared development environment through `.devcontainer`.
5. From the repository root, start the development server:
   `python -m uvicorn src.app:app --reload`.
6. Visit http://localhost:8000 for the website or http://localhost:8000/docs
   for the API documentation. The application seeds sample data into an empty
   database. Use sample data for development, and keep student information,
   passwords, and local configuration out of commits and public issues.

## Making Changes

1. Check existing issues and discuss larger changes before starting.
2. Create a branch with a descriptive name, such as `art-gallery-feature`
   or `fix-chess-signup`.
3. Make focused changes and test the affected behavior with sample data.
4. Push your branch and open a pull request describing the problem, your
   change, and how you checked it. Include screenshots for visual changes.
5. Wait for automated checks and any required code owner review, then address
   feedback before merging. The default branch requires pull requests.

## Code Style

- Follow PEP 8 for Python backend code.
- Use clear, descriptive names, such as `student_name` and `start_time`.
- Explain non-obvious logic with comments.
- Keep changes consistent with the surrounding code.

## Code Ownership and Repository Access

`CODEOWNERS` identifies the maintainer for core functionality and frontend
files. Once present on the base branch, GitHub requests reviews from the
appropriate owners. The `Protect main` ruleset requires code owner review
where applicable, blocks force pushes and deletion, and requires pull requests
for `main` and the default branch.

In a personal repository, invited collaborators receive write access while
the owner controls administrative settings. Organization repositories support
teams and more granular roles, including read, triage, write, maintain, and
admin. Grant access according to each person's responsibilities.

## Need Help or Have Ideas?

- Check open issues first. Add context to an existing issue when relevant;
  otherwise create a bug report or feature request with the provided template.
- The exercise's fictional IT Club office hours are Thursdays at lunch in
  Room 203; its example contact is `techclub@mergingtonhigh.example.edu`.
- Follow `CODE_OF_CONDUCT.md` in discussions and reviews.
- Report security concerns privately using the process in `SECURITY.md`.
