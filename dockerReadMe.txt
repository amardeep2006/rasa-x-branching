docker pull rasa/rasa-sdk:2.4.1
docker build -t amardeep2006/rasa-sdk:2.4.1 .

docker push amardeep2006/rasa-sdk:2.4.1


Run octant in the background
$ OCTANT_LISTENER_ADDR=0.0.0.0:8002 octant --disable-open-browser &

Create namespace
$ kubectl create namespace rasa-namespace

DEPLOY rasa-x with all defaults
$ helm repo add rasa-x https://rasahq.github.io/rasa-x-helm

helm --namespace rasa-namespace install --values values.yml my-release rasa-x/rasa-x


 curl -k -H "Content-Type: application/json" -X PUT --data-binary @tmp.json http://127.0.0.1:8001/api/v1/namespaces/my-namespace/finalize