# Wordpress Helm fork from Bitnami Wordpress Helm for S3 volumes

This is based on, built from the Bitnami Wordpress Helm chart (as tar file) v 17.1.15

The goal it to extend the chart to support mapping an object store (AWS S3, Min.io, Ceph) as the
ReadWriteMany volume.
