# EventStore on Google Kubernetes Engine (GKE)

This is not production ready due to it only having 1 replica.

## Running?

```
$ kubectl apply -f *.yml
```

### Reading Logs

```
$ kubectl -n eventstore logs eventstore-server-0
```

### cURL Web UI

```
$ kubectl run -it --rm --restart=Never eventstore-curl --image=appropriate/curl http://eventstore-svc.eventstore.svc.cluster.local:2113/web/index.html
```

## Why GKE?

I have tested this only on GKE and the `storage.yml` is specific to GKE.

## Future?

I'd like to either see a Chart made for EventStore on Kubernetes or create one when I understand more.
Have more then 1 replica running.

## Contributing

I hope someone with more knowledge then me is able to come along and contribute, PRs and discussions are always welcome.
