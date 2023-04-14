build-local:
	docker build -f Dockerfile -t testwebserver .

run-local:
	docker run --name=testwebserver --restart unless-stopped -p 5000:5000 -d -t testwebserver

clean-local:
	docker container stop testwebserver  || true
	docker container rm testwebserver || true

test1:
	curl -X POST  -H "Content-Type: application/JSON" --data '["Containers are more or less interesting"]' http://0.0.0.0:5000/predict

test2:
	curl -X POST  -H "Content-Type: application/json" \
  --data '["MLOps is critical for robustness"]' \
  http://0.0.0.0:5000/predict