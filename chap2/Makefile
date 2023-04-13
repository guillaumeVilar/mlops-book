build-local:
	docker build -f Dockerfile -t testwebserver .

run-local:
	docker run --name=testwebserver --restart unless-stopped -p 8080:8080 -d -t testwebserver

lint-local:
	docker container run testwebserver pylint --disable=R,C hello.py

test-local:
	docker container run testwebserver python -m pytest -vv test_hello.py

# Trigger cloudbuild: 
cloud-build:
	cd .. && gcloud builds submit --config chap2/cloudbuild.yaml
