gen-server:
	poetry run fastapi-codegen --input ../openapi.json --output-model-type pydantic_v2.BaseModel --output ../server/ap_server --generate-routers --disable-timestamp
	poetry run autoflake -i -r --remove-all-unused-imports --expand-star-imports --ignore-pass-statements ../server/ap_server
	rm ../server/ap_server/dependencies.py
	sed -i '' 's|from \.\.dependencies|from ..models|g' ../server/ap_server/routers/*.py
	sed -i '' 's|Action1|Action|g' ../server/ap_server/routers/*.py
	sed -i '' 's|from fastapi import APIRouter|from typing import Annotated\n\nfrom fastapi import APIRouter, Query|g' ../server/ap_server/routers/store.py
	sed -i '' 's|namespace: Optional\[Namespace\] = None|namespace: Annotated\[list\[str\] \| None, Query\(\)\] = None|g' ../server/ap_server/routers/store.py
	sed -i '' 's|response_model=None,|response_model=None, status_code=204,|g' ../server/ap_server/routers/*.py
	poetry run ruff format ../server/ap_server
	touch ../server/ap_server/__init__.py
	touch ../server/ap_server/routers/__init__.py

gen-client-python:
	docker run --rm -v "${PWD}/..:/local" openapitools/openapi-generator-cli generate \
    -i /local/openapi.json \
    -g python \
    -o /local/client-python \
    --package-name=ap_client
	sed -i '' 's|elif klass == object|elif klass is object|g' ../client-python/ap_client/*.py
	poetry run ruff format ../client-python/ap_client
	poetry run ruff check --fix --unsafe-fixes ../client-python/ap_client
