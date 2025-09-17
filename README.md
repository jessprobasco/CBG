# CBG

# 0) From your repo root
git clone git@github.com:jessprobasco/CBG.git
cd CBG

# 1) Create a virtualenv (keeps your Python clean)
python3 -m venv .venv
source .venv/bin/activate           # Windows: .venv\Scripts\activate

# 2) Install the same deps you use in CI
pip install --upgrade pip
pip install mkdocs mkdocs-material  # add any plugins you use

# 3) Run the local server (auto-reloads on save)
mkdocs serve
# → open http://127.0.0.1:8000