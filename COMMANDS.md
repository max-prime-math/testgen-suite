# Commands

Use these as the default entry points when working in each repo.

## Root Workspace

- `./workspace-git status`
- `./workspace-git add WORKSPACE_OVERVIEW.md CURRENT_STATE.md COMMANDS.md DECISIONS.md PROMPT_BOOTSTRAP.md`
- `./workspace-git commit -m "Update workspace docs"`
- `./workspace-git remote add origin <github-url>`
- `./workspace-git push -u origin main`
- `node scripts/update-workspace-state.mjs`

## bnk-decoder

- `npm install`
- `npm run dev`
- `npm run check`
- `npm run build`

## test-generator

- `npm install`
- `npm run dev`
- `npm run check`
- `npm run build`
- `npm run regression`

## ocr-mcq

- `python -m venv .venv`
- `source .venv/bin/activate`
- `pip install -r requirements.txt`
- `streamlit run app.py`
- `python src/main.py --input input_pdfs --output output_tex --combine`
- `python src/main.py --input input_pdfs --review`
- `pytest tests/ -v`

## ocr-frq

- `python -m pip install -r requirements.txt`
- `python -m src.main`
- `python -m src.main --years 2018,2019`
- `python -m src.main --no-form-b`
