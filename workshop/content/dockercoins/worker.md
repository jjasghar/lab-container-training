The worker has an infinite loop, that retries 10 seconds after an error

1. Stream the worker's logs

```execute
kubectl logs deploy/worker --follow
```

Wait for the `webui` service to get an `EXTERNAL-IP`.  You'll see it in the watch command output in the second terminal window.
