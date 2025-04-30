Update `pyproject.toml` to specify the new version of `chrome-devtools-protocol`
from the `python-chrome-devtools-protocol` repository.


Run:
``` bash
poetry update
poetry run make
git commit --all -m "Update for Chrome-NNN"
git tag 0.7.3+wmc
git push --tags origin
poetry publish -r dev --build # build and push to dev index for testing
poetry publish -r wqa # push to QA index for release
```
