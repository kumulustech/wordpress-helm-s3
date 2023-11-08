# Wordpress Helm fork from Bitnami Wordpress Helm for S3 volumes

This is based on, built from the Bitnami Wordpress Helm chart (as tar file) v 17.1.15

The goal it to extend the chart to support mapping an object store (AWS S3, Min.io, Ceph) as the
ReadWriteMany volume.


## Install this chart

You'll want to configure this chart to install a WordPress instance along with a Mysql database (default).

Create a values.yaml document for your particular app:

```
wordpressUsername: admin
wordpressPassword: admin
wordpressEmail: admin@example.com
service:
  type: ClusterIP
  ports:
    http: 80
```

And then install from the repository:

```
helm install wordpress-app wordpress --repo https://kumulustech.github.io/wordpress-helm-s3 --values values.yaml
```

## Contributing

Fork and submit a pull request.  We follow the code of conduct outlined in our [Code of Conduct](CODEOFCONDUCT.md) file in the root directory of the repository.
