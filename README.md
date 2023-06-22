```
diff --git 1/kustomize/build.yaml 2/kustomize5/build.yaml
index faa25b4..8d3e899 100644
--- 1/kustomize/build.yaml
+++ 2/kustomize5/build.yaml
@@ -14,7 +14,7 @@ spec:
         name: elastic
       version: ^7.0.0
   interval: 1h0m0s
-  releaseName: logstash-index-apfeed-sqs-awsqa
+  releaseName: logstash-index-apfeed-sqs
   values:
     antiAffinity: hard
     extraVolumeMounts:
@@ -115,8 +115,6 @@ spec:
             action                       => "create"
           }
         }
-    rbac:
-      create: true
     securityContext:
       readOnlyRootFilesystem: true
       runAsGroup: 1000
@@ -138,7 +136,7 @@ spec:
         name: elastic
       version: ^7.0.0
   interval: 1h0m0s
-  releaseName: logstash-index-apfeed-sqs-capdev
+  releaseName: logstash-index-apfeed-sqs
   values:
     antiAffinity: hard
     extraVolumeMounts:
@@ -239,8 +237,6 @@ spec:
             action                       => "create"
           }
         }
-    rbac:
-      create: true
     securityContext:
       readOnlyRootFilesystem: true
       runAsGroup: 1000
```
